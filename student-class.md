# Example: Student Class

## What it demonstrates
This example shows a class, fields, a constructor, an object, and a method.

```csharp
class Student
{
    public string Name;
    public int Age;

    // Constructor: gives the new object its starting values.
    public Student(string name, int age)
    {
        Name = name;
        Age = age;
    }

    // Method: an action the object can perform.
    public void Introduce()
    {
        Console.WriteLine($"My name is {Name} and I am {Age}.");
    }
}

// Create an object and call its method.
Student student = new Student("Riley", 19);
student.Introduce();
```

## Expected output

```text
My name is Riley and I am 19.
```

## Key points
- `Student` is the class name.
- `Name` and `Age` are fields.
- `Student(string name, int age)` is the constructor.
- `student` is an object variable.
- `Introduce()` is a method.
