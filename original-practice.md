# Original Practice Problems

These are self-made review exercises, not questions from a class test or exam. Try each one before checking the worked solution.

## Problem 1: Create an object
Given this class, create a `Book` object and set its title to `"Dune"`.

```csharp
class Book
{
    public string Title;
}
```

### Worked solution

```csharp
Book book = new Book();
book.Title = "Dune";
Console.WriteLine(book.Title);
```

Output: `Dune`

## Problem 2: Read a property
What does `get` do in this property?

```csharp
public int Score { get; set; }
```

### Worked solution
`get` lets code read the current value of `Score`. `set` lets code assign a new value.

## Problem 3: Enum values
What is the default numeric value of `Medium`?

```csharp
enum Size
{
    Small,
    Medium,
    Large
}
```

### Worked solution
`Medium` is `1`: the first member starts at `0`, and each next member increases by one.

## Problem 4: Tuple element
What is printed?

```csharp
(string city, int zip) location = ("Mattoon", 61938);
Console.WriteLine(location.city);
```

### Worked solution
It prints `Mattoon`, because `city` is the name of the first tuple element.
