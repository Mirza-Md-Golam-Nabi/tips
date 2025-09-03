# Form

[Back](./..)

- [Composer Package Install](#composer-package-install-)
- [Composer Auto Load](#composer-auto-load-)

## Composer Package Install ([⬆️](#form))

All packages from **require** and **require-dev** will be installed when you run this command.

```sh
composer install
```

**N.B.** Normally, this command is run in **Local**.

In production, run this command to optimize class loading and skip dev packages.

```sh
composer install --optimize-autoloader --no-dev
```

**N.B:** Normally, this command is run in **Production**.

## Composer Auto Load ([⬆️](#form))

Regenerates the autoload files (useful when you add new classes)

```sh
composer dump-autoload
```

**N.B.** Normally, it is used in **Development** environments.

Regenerates the autoload files with optimized classmap, which makes class loading faster (recommended for production).

```sh
composer dump-autoload -o
```

**N.B.** Normally, it is used in **Production** environments.


Thank you for staying with me.  
Please follow and subscribe to my YouTube channel: [YouTube Channel Link](https://www.youtube.com/@MirzaMdGolamNabi)
