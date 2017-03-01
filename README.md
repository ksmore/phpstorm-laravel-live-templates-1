# Laravel Blade - Live Templates for PhpStorm
Rework of the famous [koomai/phpstorm-laravel-live-templates](https://github.com/koomai/phpstorm-laravel-live-templates), inspired by [Lykegenes/laravel-5-snippets](https://github.com/Lykegenes/laravel-5-snippets) and [dev4dev/blade-snippets](https://github.com/dev4dev/blade-snippets) for Sublime Text 3

## How to:

1) Download and copy the *xml* file(s) to your templates folder:

* Windows: `<your home directory>\.<product name><version number>\config\templates` (create if it is not here)
* Linux: `~\.<product name><version number>\config\templates`
* OS X: `~/Library/Preferences/<product name><version number>/templates`

e.g. `C:\Users\<user>\.PhpStorm2017.1\config\templates` on Windows 10 for PhpStorm 2017.1


2) Restart PhpStorm.

3) To see all templates, go to *Preferences->Live Templates* and expand the Template Group.

Live templates show up automatically as you type the first few letters. 
You should still press `Cmd + J` to filter out everything else (classes, variables, etc).

## Template Groups

1) Blade

> Please note that each Blade template require `@` sign before. 

name="@asset"
value="{{ asset('$ASSET_PATH$') }}$END$"
description="Blade - asset()"

name="@can"
value="@can ('$POLICY$', $MODEL$)&#10;    $END$&#10;@endcan"
description="Blade - @can"

name="@canelse"
value="@can ('$POLICY$', $MODEL$)&#10;    $EXPRESSION$&#10;@else&#10;    $END$&#10;@endcan"
description="Blade - @can @else"

name="@cannot"
value="@cannot ('$POLICY$', $MODEL$)&#10;    $EXPRESSION$&#10;@else&#10;    $END$&#10;@endcannot"
description="Blade - @cannot @else"

name="@choice"
value="@choice('$LANGUAGE_LINE$', $NUMBER$)$END$"
description="Blade - @choice"

name="@continue"
value="@continue$END$"
description="Blade - @continue"

name="@each"
value="@each('$ITEM_VIEW$', $ITEMS$, '$ITEM$', '$EMPTY_VIEW$')$END$"
description="Blade - @each"

name="@extends"
value="@extends('$VIEW$')$END$"
description="Blade - @extends"

name="@for"
value="@for ($VARIABLE$ = $START_COUNT$; $VARIABLE$ &lt; $COUNT$; $VARIABLE$++)&#10;   $END$&#10;@endfor"
description="Blade - @for"

name="@fore"
value="@forelse ($ARRAY$ as $ELEMENT$)&#10;    $EXP$&#10;@empty&#10;    $END$&#10;@endforelse"
description="Blade - @forelse @empty"

name="@foreach"
value="@foreach ($ARRAY$ as $ELEMENT$)&#10;    $END$&#10;@endforeach"
description="Blade - @foreach"

name="@if"
value="@if ($CONDITION$)&#10;   $END$&#10;@endif"
description="Blade - @if"

name="@ifelse"
value="@if ($CONDITION$)&#10;   $EXP$&#10;@else&#10;   $END$&#10;@endif"
description="Blade - @if @else"

name="@inc_data"
value="@include('$VIEW$', ['$DATA$' =&gt; $$$DATA$])$END$"
description="Blade - @include with data"

name="@include"
value="@include('$VIEW$')$END$"
description="Blade - @include"

name="@inject"
value="@inject('$NAME$', '$SERVICE$')$END$"
description="Blade - @inject"

name="@lang"
value="@lang('$LINE$')$END$"
description="Blade - @lang"

name="@lang_json"
value="{{ __('$LINE$') }}$END$"
description="Blade - __()"

name="@lang_rep"
value="@lang('$LINE$', ['$VARIABLE$' =&gt; $VALUE$])$END$"
description="Blade - @lang with data"

name="@section"
value="@section ('$SECTION$')&#10;    $END$&#10;@stop"
description="Blade - @section"

name="@section_inline"
value="@section('$SECTION$', $CONTENT$)$END$"
description="Blade - Inline @section"

name="@layout"
value="@layout('$SECTION$')$END$"
description="Blade - @layout"

name="@yield"
value="@yield('$CONTENT$'$DEFAULT$)$END$"
description="Blade - @yield"

name="@trans"
value="{{ trans('$LINE$') }}$END$"
description="Blade - trans()"

name="@unless"
value="@unless ($CONDITION$)&#10;    $END$&#10;@endunless"
description="Blade - @unless"

name="@url"
value="{{ url('$LINE$') }}$END$"
description="Blade -url()"

name="@csrf"
value="{{ csrf_field() }}$END$"
description="Blade - csrf_field()"

name="@while"
value="@while ($CONDITION$)&#10;    $END$&#10;@endwhile"
description="Blade - @while"

name="@push"
value="@push('$START$')&#10;    $END$&#10;@endpush"
description="Blade - @push"

name="@php"
value="@php&#10;    $END$&#10;@endphp"
description="Blade - @php"

name="@stack"
value="@stack('$NAME$')$END$"
description="Blade - @stack"

name="{!!"
value="{!! $START$ !!}$END$"
description="Blade {!! echo raw data !!}"

name="{{"
value="{{ $START$ }}$END$"
description="Blade {{ echo data }}"

name="{{--"
value="{{-- $START$ --}}$END$"
description="Blade comment"

name="@route"
value="{{ route('$NAME$') }}$END$"
description="Blade - route()"


2) Package Specific

> This group contains all templates maded for specific packages. This is an optional package. 
> This is a templates for my packages of choice. If you have your own stack of packages, please make templates by yourself.

name="@spaceless"
@spaceless&#10;$END$&#10;@endspaceless"
Blade - @spaceless [slydeath/laravel5-blade-spaceless](https://github.com/SlyDeath/laravel5-blade-spaceless)"

name="@group"
@group ('$GROUP$')&#10;    $END$&#10;@endgroup"
Blade - @group [httpoz\roles](https://github.com/httpoz/roles)"

name="@role"
@role ('$ROLE$')&#10;    $END$&#10;@endrole"
Blade - @role [httpoz\roles](https://github.com/httpoz/roles)"


## Master plan
- [ ] Rework all the templates in [koomai/phpstorm-laravel-live-templates](https://github.com/koomai/phpstorm-laravel-live-templates)
 - [ ] Annotations
 - [x] Blade
 - [ ] Input
 - [ ] Request
 - [ ] Cookie
 - [ ] Route
 - [ ] View
 - [ ] Response
 - [ ] Redirect
 - [ ] Schema
 - [ ] Cache
 - [ ] Form
 - [ ] Session
 - [ ] Helpers
- [ ] Rework the documentation
