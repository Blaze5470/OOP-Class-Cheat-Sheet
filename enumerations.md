# Enumerations (Enums)

An **enum** is a value type that defines a set of named constants. It makes code easier to read than unexplained numbers.

```csharp
enum Day
{
    Monday,
    Tuesday,
    Wednesday,
    Thursday,
    Friday
}

Day today = Day.Monday;
```

## Default numeric values
By default, enum members use `int`. The first member is `0`, and each following member increases by one.

```csharp
enum Level
{
    Low,    // 0
    Medium, // 1
    High    // 2
}
```

You can assign values yourself:

```csharp
enum Status
{
    New = 1,
    Active = 5,
    Complete = 10
}
```

## Remember
- Use `EnumType.Member`, such as `Day.Friday`.
- Enum members are named constants.
- Enums are useful for a fixed set of related choices.
