# Installation

[Back](./..)

- [Laragon Install](#laragon-install-%EF%B8%8F)
- [Composer Install](#composer-install-%EF%B8%8F)
- [phpMyAdmin Install in Laragon](#phpmyadmin-install-in-laragon-%EF%B8%8F)
- [7 Zip Install](#7-zip-install-%EF%B8%8F)
- [Node js Install](#node-js-install-%EF%B8%8F)
- [Laravel Install](#laravel-install-%EF%B8%8F)
- [Livewire Install](#livewire-install-%EF%B8%8F)
- [Vue Install](#vue-install-️)

## Laragon Install ([⬆️](#installation))

Laragon provides a beautiful server environment, but it is not free software.  
If you want to install Laragon on your PC, visit the following URL to download and install it:

```sh
https://laragon.org/download
```

N.B: **If you want to know more details about Laragon, go to this link**

[Laragon](./laragon/README.md)

## Composer Install ([⬆️](#installation))

Composer is a Dependency Manager for PHP that simplifies library and package management. ✅
If you want to install Composer on your PC, visit the following URL to download and install it:

```sh
https://getcomposer.org/download
```

N.B: **If you want to know more details about Composer, go to this link**

[Composer](./composer/README.md)

## phpMyAdmin Install in Laragon ([⬆️](#installation))

Click on the link below and see how to install phpMyAdmin in Laragon (with images). ✅

[phpMyAdmin](./phpMyAdmin/README.md)

## 7 Zip Install ([⬆️](#installation))

If you face an unzip problem while downloading a Laravel application on your local machine, you can download and install the "7-Zip" software.

Click on the link below to see how to install 7-Zip on your system with images. ✅

[7 Zip](./7zip/README.md)

## Node js Install ([⬆️](#installation))

Click on the link below and see how to install Nodejs on your local machine with images. ✅

[Node JS](./nodejs/README.md)

## Laravel Install ([⬆️](#installation))

**Applicable for Laravel 11 or later versions.**<br>

Before creating your first Laravel application, make sure that your local machine has PHP, Composer, and the Laravel installer installed. In addition, you should install Node and NPM so that you can compile your application's frontend assets.

#### 1. Check whether PHP is installed or not.

```sh
php --version
```

**N.B. If you see the PHP version, then PHP is installed successfully.** If PHP is not installed, then install [Laragon](./laragon/README.md). It is easy for windows user.

#### 2. Check whether composer is installed or not.

```sh
composer --version
```

**N.B. If you see the Composer version, then Composer is installed successfully.** If Composer is not installed, then install [Composer](./composer/README.md).

#### 3. Check whether Laravel installer is installed or not.

```sh
laravel --version
```

**N.B. If you see the Laravel installer version, then Laravel installer is installed successfully.** If Laravel installer is not installed, then run this command in your terminal.

```sh
composer global require laravel/installer
```

#### 4. Creating Laravel Application

After you have installed PHP, Composer, and the Laravel installer, you're ready to create a new Laravel application. Run this command:

```sh
laravel new project-name
```

The Laravel installer will prompt you to select your preferred testing framework, database, and starter kit.

## Livewire Install ([⬆️](#installation))

Livewire is a Laravel package, so you will need to have a Laravel application up and running before you can install and use Livewire.

To install Livewire, open your terminal and navigate to your Laravel application directory, then run the following command:

```sh
composer require livewire/livewire
```

## Vue Install ([⬆️](#installation))

Run this command:

```sh
npm install vue vue-router @vitejs/plugin-vue
```

- **vue** = Vue install
- **vue-router** = Vue routing library
- **@vitejs/plugin-vue** = A quick build tool

Config your **_vite.config.js_** file

```sh
import { defineConfig } from 'vite';
import laravel from 'laravel-vite-plugin';
import tailwindcss from '@tailwindcss/vite';
import vue from "@vitejs/plugin-vue";

export default defineConfig({
    plugins: [
        vue(),
        laravel({
            input: [
                'resources/css/app.css',
                'resources/js/app.js'
            ],
            refresh: true,
        }),
        tailwindcss(),
    ],
    resolve: {
        alias: {
            "@": "/resources/js",
            vue: "vue/dist/vue.esm-bundler.js",
        },
    },
});
```

**Added vue() and resolve**

The resolve.alias section defines shortcuts:

- **@** maps to /resources/js for cleaner imports
- **vue** points to vue.esm-bundler.js for proper Vue bundling

**If you want to read more, click this [Link](./vue/README.md)**

Thank you for staying with me.  
Please follow and subscribe to my YouTube channel: [YouTube Channel Link](https://www.youtube.com/@MirzaMdGolamNabi)
