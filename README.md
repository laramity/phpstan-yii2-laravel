# Yii2 extension for PHPStan

[![Minimum PHP Version](https://img.shields.io/badge/php-%3E%3D%207.2-8892BF.svg)](https://php.net/)
[![Latest Stable Version](https://img.shields.io/packagist/v/miserenkov/phpstan-yii2-laravel.svg)](https://packagist.org/packages/miserenkov/phpstan-yii2-laravel)
[![Build Status](https://github.com/miserenkov/phpstan-yii2-laravel/workflows/build/badge.svg)](https://github.com/miserenkov/phpstan-yii2-laravel/actions?query=workflow%3Abuild)
[![Total Downloads](https://poser.pugx.org/miserenkov/phpstan-yii2-laravel/downloads.svg)](https://packagist.org/packages/miserenkov/phpstan-yii2-laravel)
[![License](https://poser.pugx.org/miserenkov/phpstan-yii2-laravel/license.svg)](https://packagist.org/packages/miserenkov/phpstan-yii2-laravel)

## What does it do?

* Provides correct return type for `Yii::$container->get('service_id')` method,
* Provides correct methods and properties for `Yii::$app->request`
* Ignore common problems with response objects (to be removed).

## Compatibility

| PHPStan version | Yii2 extension version |
|-----------------|------------------------|
| 1.x             | 0.8.x                  |
| 0.12            | 0.7.x                  |
| 0.11            | 0.5.x - 0.6.x          |
| 0.10.3          | 0.4.x                  |
| 0.10            | 0.3.0                  |
| 0.9.2           | 0.2.0                  |

## Installation

```sh
composer require --dev miserenkov/phpstan-yii2-laravel
```

## Configuration

Put this into your `phpstan.neon` config:

```neon
includes:
	- vendor/miserenkov/phpstan-yii2-laravel/extension.neon
parameters:
    yii2:
        application_id: api
```

## Limitations

Container closures must have return types.

You have to provide config for yii application in laravel application in key yii.{application_id}
