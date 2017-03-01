# Laravel - Live Templates for PhpStorm
Rework of the famous [koomai/phpstorm-laravel-live-templates](https://github.com/koomai/phpstorm-laravel-live-templates), inspired by [Lykegenes/laravel-5-snippets](https://github.com/Lykegenes/laravel-5-snippets) and [dev4dev/blade-snippets](https://github.com/dev4dev/blade-snippets) for Sublime Text 3
Based on Laravel >= 5.3

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
- [Blade](#blade)
- [Package Specific](#package-specific)


### Blade

> Please note that each Blade template require `@` sign before. 

- **@asset** - `asset()` in curly braces

```php
{{ asset('$ASSET_PATH$') }}
```


- **@can** - simple `@can` 

```php
@can ('policy', App\Model)
@endcan
```

- **@canelse** - `@can` with `@else`

```php 
@can ('policu', App\Model)
@else
@endcan
```

 - **@cannot** - `@cannot` with `@else`
 
```php 
@cannot ('policy', App\Model)
@else
@endcannot
```

- **@choice**

```php
@choice('lang.line', $number)
```

- **@continue**

```php
@continue
```

- **@each**

```php
@each('item.view', $items, 'item', 'empty.view')
```

- **@extends**

```php
@extends('view')
```

- **@for**

```php
@for ($i = $start; $i > $count; $i++)
@endfor
```

- **@fore** - `@forelse` with  `@empty`

```php
@forelse ($array as $element)
@empty
@endforelse
```

- **@foreach**

```php
@foreach ($array as $element)
@endforeach
```

- **@if**

```php
@if (condition)
@endif
```

- **@ifelse**
```php
@if (condition)
@else
@endif
```

- **@include** - simple `@include`

```php
@include('view')
```

- **@inc_data** - `@include` with data array

```php
@include('view', ['data' => $data])
```

- **@inject**

```php
@inject('name', 'App\Services\ServiceName')
```

- **@lang**

```php
@lang('line')
```

- **@lang_rep** - @lang with data

```php
@lang('line', ['variable' => $value])
```

- **@lang_json** - `__()` helper

```php
{{ __('line') }}
```

- **@section** - simple `@section`

```php
@section ('section')
@stop
```

- **@section_inline** - Inline `@section`

```php
@section('section', $content)
```

- **@layout**

```php
@layout('section')
```

- **@yield**

```php
@yield('content')
```

- **@trans** - `trans()` helper

```php
{{ trans('line') }}
```

- **@unless**

```php
@unless (condition)
@endunless
```

- **@url** - `url()` helper

```php
{{ url('line') }}
```

- **@csrf** - `csrf_field()` (+ one empty lane after)

```php
{{ csrf_field() }}

```

- **@while**

```php
@while (condition)
@endwhile
```

- **@push**

```php
@push('scripts')
@endpush
```

- **@stack**
```php
@stack('scripts')
```

- **@php**

```php
@php
@endphp
```

- **{!!** - {!! raw data !!} (might be in conflict with internal Blade block tags)
```php
{!! bla !!}
```

- **{{** - {{ data }} (might be in conflict with internal Blade block tags)
```php
{{ bla }}
```

- **{{--** - comment (might be in conflict with internal Blade block tags)
```php
{{-- bla --}}
```

- **@route** - `route()` helper
```php
{{ route('route.name') }}
```



### Package Specific

> This group contains all templates made for specific packages. This is an optional group. 
> It has templates for my packages of choice. If you have your own stack of packages, please make templates by yourself.

- **@spaceless** - Blade `@spaceless` for [slydeath/laravel5-blade-spaceless](https://github.com/SlyDeath/laravel5-blade-spaceless)
```php
@spaceless
@endspaceless
```

- **@group** - Blade `@group` for [httpoz\roles](https://github.com/httpoz/roles)

```php
@group ('group_name')
@endgroup
```

- **@role** - Blade `@role` for [httpoz\roles](https://github.com/httpoz/roles)

```php
@role ('role_name')
@endrole
```

_____


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
