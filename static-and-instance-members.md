# Static and Instance Members

## Static
A **static** member belongs to the type itself, not to one particular object.

```csharp
class Calculator
{
    public static int Add(int a, int b)
    {
        return a + b;
    }
}

int answer = Calculator.Add(5, 3);
```

Call the method using the class name. You do not need a `Calculator` object.

## Instance
An instance member belongs to an individual object.

```csharp
class Player
{
    public string Name;

    public void SayName()
    {
        Console.WriteLine(Name);
    }
}

Player player = new Player();
player.Name = "Kai";
player.SayName();
```

## Static fields
A static field is shared by the type rather than having a separate copy for each object.

```csharp
class Player
{
    public static int PlayerCount = 0;

    public Player()
    {
        PlayerCount++;
    }
}
```

## Comparison

| Instance member | Static member |
|---|---|
| Belongs to an object | Belongs to the type |
| Accessed through an object | Usually accessed through the type name |
| Each object has its own instance field | One shared static field per type |

A static method cannot directly use an instance field or instance method because it does not have a particular object (`this`) to use.
