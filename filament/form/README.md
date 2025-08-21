# Form

[Back](./..)

- [Remove CreateAnother Button](#remove-createanother-button-️)
- [Inline Label Position](#inline-label-position-️)

## Remove CreateAnother Button ([⬆️](#form))

<img src="./images/createAnother.png">

```php
class ManageCustomers extends ManageRecords
{
    protected static string $resource = CustomerResource::class;

    protected function getHeaderActions(): array
    {
        return [
            Actions\CreateAction::make()
                ->createAnother(false),
        ];
    }
}
```

Or

You can use another way for **create page**

```php
protected static bool $canCreateAnother = false;
```

## Inline Label Position ([⬆️](#form))

<img src="./images/inlineLabel.png">

```php
use Filament\Forms\Components\Radio;

Radio::make('feedback')
    ->label('Like this post?')
    ->options([
        '1' => 'Yes',
        '0' => 'No',
    ])
    ->inline()
    ->inlineLabel(false),
```

Thank you for staying with me.  
Please follow and subscribe to my YouTube channel: [YouTube Channel Link](https://www.youtube.com/@MirzaMdGolamNabi)
