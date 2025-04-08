# Installation

[Back](./..)

- [Laragon Install](#laragon-install-️)
- [Composer Install](#composer-install-️)
- [PHP Install in Laragon](#php-install-in-laragon-️)
- [phpMyAdmin Install in Laragon](#phpmyadmin-install-in-laragon-️)
- [7 Zip Install](#7-zip-install-️)
- [Node js Install](#node-js-install-️)
- [Laravel Install](#laravel-install-️)
- [Livewire Install](#livewire-install-️)
- [Vue Install](#vue-install-️)
- [Bootstrap Install in Vue](#bootstrap-install-in-vue-️)
- [Bootstrap Install in Livewire](#bootstrap-install-in-livewire-️)

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

## PHP Install in Laragon ([⬆️](#installation))

Click on the link below and see how to install **PHP** in Laragon (with images). ✅

[PHP](./php/README.md)

## phpMyAdmin Install in Laragon ([⬆️](#installation))

Click on the link below and see how to install **phpMyAdmin** in Laragon (with images). ✅

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

## Bootstrap Install in Vue ([⬆️](#installation))

If you want to install **Bootstrap** in your **Laravel** with **Vue** project, then run this command:

```sh
npm install bootstrap
```

After complete the installation, then import it in your **resources/js/app.js** file.

```sh
import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap';
```

**If you want to read more, click this [Link](./bootstrap/README.md/#bootstrap-install-in-vue-️)**

## Bootstrap Install in Livewire ([⬆️](#installation))

If you want to install **Bootstrap** in your **Laravel** with **Livewire** project, then run this command:

```sh
npm install bootstrap @popperjs/core
```

After complete the installation, then import **Bootstrap** in your **resources/css/app.css** file.

```sh
@import 'bootstrap';
```

Then also import **Bootstrap** in your **resources/js/app.js** file.

```sh
import 'bootstrap';
```

Set path in the **vite.config.js** file

```sh
export default defineConfig({
    plugins: [laravel({
        input: ['resources/css/app.css', 'resources/js/app.js'],
        refresh: true,
    })],
});
```

Link CSS and JS in Blade file:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    @vite(['resources/css/app.css', 'resources/js/app.js'])
  </head>
  <body></body>
</html>
```

Now, finally run this command:

```sh
npm run dev
```

✅ Now, you can enjoy bootstrap in your code. 😎

**If you want to read more, click this [Link](./bootstrap/README.md/#bootstrap-install-in-livewire-️)**

Thank you for staying with me.  
Please follow and subscribe to my YouTube channel: [YouTube Channel Link](https://www.youtube.com/@MirzaMdGolamNabi)
