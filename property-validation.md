# Example: Property Validation

## What it demonstrates
A property can check a value before storing it.

```csharp
class Product
{
    private decimal price;

    public decimal Price
    {
        get { return price; }
        set
        {
            if (value >= 0)
                price = value;
        }
    }
}

Product item = new Product();
item.Price = 12.50m;
Console.WriteLine(item.Price);
```

## Expected output

```text
12.50
```

## Key points
- `price` is a private backing field.
- `Price` is the public property.
- `get` returns the stored value.
- `set` receives the new value through `value`.
- The condition prevents a negative value from being stored.

The `m` suffix makes `12.50m` a `decimal` literal.
