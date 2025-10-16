# Composer

[Back](./..)

- [Composer Package Install](#composer-package-install-%EF%B8%8F)
- [Composer install in cPanel](#composer-install-in-cpanel-%EF%B8%8F)
- [Composer Auto Load](#composer-auto-load-%EF%B8%8F)

## Composer Package Install ([⬆️](#composer))

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

## Composer Install in cPanel ([⬆️](#composer))

If you want to install composer in cPanel, first check **composer** is install or not. For checking:

```sh
composer -v
```

If you see "**Composer Not Found**", then check which PHP version is available in your system.

```sh
ls /opt/cpanel/ea-php*
```

After running this command, it shows like this:
> ea-php80  ea-php81  ea-php82  ea-php83  ea-php84

Then check the version:

```sh
/opt/cpanel/ea-php83/root/usr/bin/php -v
```

If it shows the PHP version, then path is **OK**

**Now go to your subdomain**

```sh
cd sub-domain-path
```

Download composer:

```sh
curl -sS https://getcomposer.org/installer | /opt/cpanel/ea-php83/root/usr/bin/php
```

you can set Alias:

```sh
alias composer="/opt/cpanel/ea-php83/root/usr/bin/php composer.phar"
```

Then run install command:

```sh
composer install
```

Or you can use the same path for composer install:

```sh
/opt/cpanel/ea-php83/root/usr/bin/php composer.phar install

```

## Composer Auto Load ([⬆️](#composer))

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
