# Page

[Back](./..)

- [Remove Item From Sidebar Menu](#remove-item-from-sidebar-menu-%EF%B8%8F)
- [Customizing the page URL](#customizing-the-page-url-%EF%B8%8F)
- [Customizing the page title](#customizing-the-page-title-%EF%B8%8F)
- [Customizing the page navigation label](#customizing-the-page-navigation-label-%EF%B8%8F)
- [Customizing the page heading](#customizing-the-page-heading-%EF%B8%8F)

## Remove item from sidebar menu ([⬆️](#page))

If you remove the item from the sidebar menu, then use this code. 

```sh
protected static bool $shouldRegisterNavigation = false;
```

## Customizing the page URL ([⬆️](#page))

By default, Filament will automatically generate a URL (slug) for your page based on its name. You may override this by defining a $slug property on your page class:

```sh
protected static ?string $slug = 'custom-url-slug';
```

## Customizing the page title ([⬆️](#page))

By default, Filament will automatically generate a title for your page based on its name. You may override this by defining a $title property on your page class:

```sh
protected static ?string $title = 'Custom Page Title';
```

## Customizing the page navigation label ([⬆️](#page))

By default, Filament will use the page’s title as its navigation item label. You may override this by defining a **$navigationLabel** property on your page class:

```sh
protected static ?string $navigationLabel = 'Custom Navigation Label';
```

## Customizing the page heading ([⬆️](#page))

By default, Filament will use the page’s title as its heading. You may override this by defining a $heading property on your page class:

```sh
protected ?string $heading = 'Custom Page Heading';
```

Dynamic **$heading** set:

```php

public function getHeading(): string
{
    $heading = CustomerEnum::from($this->c_type_id)->bangla() . " customer";

    return __($heading);
}

```


Thank you for staying with me.  
Please follow and subscribe to my YouTube channel: [YouTube Channel Link](https://www.youtube.com/@MirzaMdGolamNabi)

