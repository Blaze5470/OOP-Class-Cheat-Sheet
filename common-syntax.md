# Common C# Syntax

## Vocabulary

| Term | Meaning |
|---|---|
| Class | Blueprint for objects |
| Object | Instance of a class |
| Field | Variable declared in a type |
| Method | Function declared in a type |
| Constructor | Initializes a new object |
| Property | Controlled access to a value |
| `get` | Reads a property |
| `set` | Assigns a property |
| `private` | Restricts access to the containing type |
| `public` | Allows accessible outside use |
| `static` | Belongs to the type |
| Enum | Group of named constants |
| Tuple | Groups multiple values |

## Syntax patterns

```csharp
// Class
class Example { }

// Create an object
Example item = new Example();

// Method
public void SayHello()
{
    Console.WriteLine("Hello");
}

// Constructor
public Example()
{
    // initialization
}

// Auto-property
public string Name { get; set; }

// Enum
enum Direction { North, South, East, West }

// Named tuple
(string name, int score) result = ("Sam", 95);

// Static method
public static int Double(int number)
{
    return number * 2;
}
```

## Useful reminders
- `.` accesses a member: `student.Name`.
- `new` creates an instance.
- `return` sends a value back from a method.
- Parameters are declared in a method definition; arguments are passed when calling it.
- Constructors have the class name and no return type.
