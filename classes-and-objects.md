# Classes and Objects

## Class
A **class** is a blueprint that describes the data and actions its objects can have.

```csharp
class Student
{
    public string Name;
    public int Age;

    public void Introduce()
    {
        Console.WriteLine($"Hi, I am {Name}.");
    }
}
```

## Object
An **object** is an instance created from a class. The `new` keyword creates it.

```csharp
Student student = new Student();
student.Name = "Avery";
student.Age = 18;
student.Introduce();
```

## Important vocabulary

| Term | Meaning |
|---|---|
| Class | Blueprint for creating objects |
| Object / instance | A value created from a class |
| Field | A variable declared in a class |
| Method | A function declared in a class |
| Constructor | Special member that runs when an object is created |
| Parameter | Variable listed in a method or constructor declaration |
| Argument | Actual value passed to a method or constructor |

## Constructors
A constructor has the same name as its class and has no return type.

```csharp
class Student
{
    public string Name;

    public Student(string name)
    {
        Name = name;
    }
}

Student student = new Student("Avery");
```

**When to use it:** Use a constructor to give a new object its starting values.

**Remember:** If you declare a constructor, C# does not automatically add a parameterless constructor for you.

## Instance members
A normal, non-static field belongs to each object separately. Two objects can store different values.

```csharp
Student first = new Student("Avery");
Student second = new Student("Jordan");
```

Each object has its own `Name`.
