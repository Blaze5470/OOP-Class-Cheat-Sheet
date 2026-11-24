# Example: Enum and Tuple

## Enum example

```csharp
enum TrafficLight
{
    Red,
    Yellow,
    Green
}

TrafficLight signal = TrafficLight.Green;
Console.WriteLine(signal);
```

Output: `Green`

## Tuple example

```csharp
(string item, int quantity) order = ("Notebook", 3);

Console.WriteLine(order.item);
Console.WriteLine(order.quantity);
```

Output:

```text
Notebook
3
```

## Key points
- `TrafficLight.Green` is a named enum value.
- The enum's default first value is numeric `0`.
- The tuple groups a string and an integer.
- Named tuple elements are accessed by their names.
