# Bootstrap

[Back](./..)

- [Bootstrap install in Vue](#bootstrap-install-in-vue-️)
- [Bootstrap install in Livewire](#bootstrap-install-in-livewire-️)
- [Bootstrap install in Laravel](#bootstrap-install-in-laravel-️)

## Bootstrap install in Vue ([⬆️](#bootstrap))

If you want to install **Bootstrap** in your **Laravel** with **Vue** project, then you run this command:

```sh
npm install bootstrap
```

After complete the installation, then import it in your **resources/js/app.js** file.

```sh
import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap';
```

✅ Now, you can enjoy bootstrap in your code. 😎

If **Bootstrap Component** (dropdowns, tooltips, popovers etc) does not work properly, then you can run this command:

```sh
npm install @popperjs/core
```

After complete the installation, then import it in your **resources/js/app.js** file.

```sh
import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap';
import '@popperjs/core';
```

✅ Now, you can enjoy bootstrap properly in your code. 😎

## Bootstrap install in Livewire ([⬆️](#bootstrap))

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

```php
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

## Bootstrap install in Laravel ([⬆️](#bootstrap))

Please read this doc [Link](../README.md/#bootstrap-install-in-laravel-️)

Thank you for staying with me.  
Please follow and subscribe to my YouTube channel: [YouTube Channel Link](https://www.youtube.com/@MirzaMdGolamNabi)
