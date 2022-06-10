# Filament Blog Builder

[![Latest Version on Packagist](https://img.shields.io/packagist/v/thianpri/filament-lab.svg?style=flat-square)](https://packagist.org/packages/thianpri/filament-blog)
[![GitHub Tests Action Status](https://img.shields.io/github/workflow/status/thianpri/filament-lab/run-tests?label=tests)](https://github.com/thianpri/filament-lab/actions?query=workflow%3Arun-tests+branch%3Amain)
[![GitHub Code Style Action Status](https://img.shields.io/github/workflow/status/thianpri/filament-lab/Check%20&%20fix%20styling?label=code%20style)](https://github.com/thianpri/filament-lab/actions?query=workflow%3A"Check+%26+fix+styling"+branch%3Amain)
[![Total Downloads](https://img.shields.io/packagist/dt/thianpri/filament-lab.svg?style=flat-square)](https://packagist.org/packages/thianpri/filament-lab)

A faceless blog content manager with configurable richtext and markdown support for filament admin panel.

![](./art/screen1.png)

## Filament Admin Panel
This package is tailored for [Filament Admin Panel](https://filamentphp.com/). 

Make sure you have installed the admin panel before you continue with the installation. You can check the [documentation here](https://filamentphp.com/docs/admin)

## Supported Versions
PHP: `8.0`

Laravel: `8` & `9`

## Installation
You can install the package via composer:

```bash
composer require thianpri/filament-lab

php artisan filament-lab:install

php artisan storage:link

php artisan migrate
```

### Configurations
This is the contents of the published config file:

```php
<?php

return [

    /**
     * Supported content editors: richtext & markdown:
     *      \Filament\Forms\Components\RichEditor::class
     *      \Filament\Forms\Components\MarkdownEditor::class
     */
    'editor'  => \Filament\Forms\Components\RichEditor::class,

    /**
     * Buttons for text editor toolbar.
     */
    'toolbar_buttons' => [
        'attachFiles',
        'blockquote',
        'bold',
        'bulletList',
        'codeBlock',
        'h2',
        'h3',
        'italic',
        'link',
        'orderedList',
        'redo',
        'strike',
        'undo',
    ],
];
```


## Displaying your content
Filment lab builder is faceless, it doesn't have any opinions on how you display your content in your frontend. You can use the lab models in your controllers to display the different resources:

- `thianpri\FilamentLab\Models\Post`
- `thianpri\FilamentLab\Models\Author`
- `thianpri\FilamentLab\Models\Category`

## Testing

```bash
composer test
```

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Contributing

Please see [CONTRIBUTING](.github/CONTRIBUTING.md) for details.

## Security Vulnerabilities

Please review [our security policy](../../security/policy) on how to report security vulnerabilities.

## Credits

- [thianpri](https://github.com/thianpri)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
