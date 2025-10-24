# Table

[Back](./..)

- [Data Format Change](#data-format-change-%EF%B8%8F)
- [ENUM use at the table](#enum-use-at-the-table-%EF%B8%8F)
- [Default sort use in the table](#default-sort-use-in-the-table-%EF%B8%8F)

## Data Format Change ([⬆️](#table))

If you want to change the format of the incoming data, then you can use this method:

```php
TextColumn::make('balance')
	->formatStateUsing(fn($state) => format_number($state) ?? 0),
```

## ENUM use at the table ([⬆️](#table))

You can use ENUM at the everywhere. Here, I give an example for 3 methods - **searchable()**, **formatStateUsing()**, and **color()**.

```php
TextColumn::make('type')
    ->searchable(query: function ($query, string $search): void {
        $matching = collect(CustomerEnum::cases())
            ->filter(fn($case) => str_contains($case->bangla(), $search))
            ->map(fn($case) => $case->value);

        $query->whereIn('type', $matching);
    })
    ->badge()
    ->formatStateUsing(fn(CustomerEnum $state) => $state->bangla())
    ->color(fn(CustomerEnum $state) => $state->color()),
```

## Default sort use in the table ([⬆️](#table))

If you want to use default sort in your table, you can use **defaultSort()** method.

```php
public function table(Table $table): Table
{
    return $table
        ->columns([
        	// Table column data
        ])
        ->defaultSort('name', 'asc'); // Use this method
}
```

Thank you for staying with me.  
Please follow and subscribe to my YouTube channel: [YouTube Channel Link](https://www.youtube.com/@MirzaMdGolamNabi)
