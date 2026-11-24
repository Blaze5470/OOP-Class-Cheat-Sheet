# Tuples

A **tuple** groups multiple values into one value. The values can have different types.

## Unnamed elements

```csharp
(string, int) student = ("Avery", 18);

Console.WriteLine(student.Item1); // Avery
Console.WriteLine(student.Item2); // 18
```

## Named elements
Names make tuple values easier to understand.

```csharp
(string name, int age) student = ("Avery", 18);

Console.WriteLine(student.name);
Console.WriteLine(student.age);
```

## Returning multiple values

```csharp
static (int sum, int difference) Calculate(int a, int b)
{
    return (a + b, a - b);
}

var result = Calculate(8, 3);
Console.WriteLine(result.sum);        // 11
Console.WriteLine(result.difference); // 5
```

## Remember
- `Item1` is the first unnamed element; `Item2` is the second.
- Named tuple elements can be accessed by name.
- Tuple elements have specific types.
