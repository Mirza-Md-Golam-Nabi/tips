# Resource

[Back](./..)

- [Modify navigation label or sidebar menu item](#modify-navigation-label-or-sidebar-menu-item-%EF%B8%8F)
- [Modify Navigation Icon](#modify-navigation-icon-%EF%B8%8F)
- [Sorting Resource Navigation Items](#sorting-resource-navigation-items-%EF%B8%8F)
- [Grouping Resource Navigation Items](#grouping-resource-navigation-items-%EF%B8%8F)

## Modify navigation label or sidebar menu item ([⬆️](#resource))

```php
protected static ?string $navigationLabel = 'Navigation Label';
```

Or

```php
public static function getNavigationLabel(): string
{
    return __('Navigation Label');
}
```

[Filament Link](https://filamentphp.com/docs/3.x/panels/resources/getting-started#resource-navigation-items)

## Modify Navigation Icon ([⬆️](#resource))

```php
protected static ?string $navigationIcon = 'heroicon-o-academic-cap';
```

Or

```php
use Illuminate\Contracts\Support\Htmlable;

public static function getNavigationIcon(): string | Htmlable | null
{
    return 'heroicon-o-user-group';
}
```

[Filament Link](https://filamentphp.com/docs/3.x/panels/resources/getting-started#setting-a-resource-navigation-icon)

## Sorting Resource Navigation Items ([⬆️](#resource))

```php
protected static ?int $navigationSort = 2;
```

Or

```php
public static function getNavigationSort(): ?int
{
    return 2;
}
```

[Filament Link](https://filamentphp.com/docs/3.x/panels/resources/getting-started#sorting-resource-navigation-items)

## Grouping Resource Navigation Items ([⬆️](#resource))

```php
protected static ?string $navigationGroup = 'Summary';
```

Or

```php
public static function getNavigationGroup(): ?string
{
    return __('Summary');
}
```

You can nest navigation items under a parent by setting the parent’s label in **$navigationParentItem**.

```php
protected static ?string $navigationParentItem = 'Products';

protected static ?string $navigationGroup = 'Shop';
```

[Filament Link](https://filamentphp.com/docs/3.x/panels/resources/getting-started#grouping-resource-navigation-items)

Thank you for staying with me.  
Please follow and subscribe to my YouTube channel: [YouTube Channel Link](https://www.youtube.com/@MirzaMdGolamNabi)
