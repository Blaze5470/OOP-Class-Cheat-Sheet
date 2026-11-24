# Information Hiding and Properties

## Information hiding
**Information hiding** means protecting the internal data of a class and providing controlled ways to use it.

- `private`: accessible only inside the containing type.
- `public`: accessible from outside, subject to the accessibility of the containing type.
- A common pattern is to keep fields private and expose public methods or properties.

```csharp
class BankAccount
{
    private decimal balance;

    public void Deposit(decimal amount)
    {
        if (amount > 0)
            balance += amount;
    }

    public decimal GetBalance()
    {
        return balance;
    }
}
```

Outside code cannot directly access `balance`.

## Properties
A **property** provides controlled access to data.

```csharp
class Student
{
    private string name;

    public string Name
    {
        get { return name; }
        set { name = value; }
    }
}
```

- `get` reads and returns the property's value.
- `set` assigns a new value.
- In a `set` accessor, `value` means the incoming value.

## Auto-properties
Use an auto-property when no extra logic is needed:

```csharp
public string Name { get; set; }
public int Age { get; private set; }
```

`get; set;` allows reading and writing. `get; private set;` allows outside code to read, but only code inside the class to set.

## Validation example

```csharp
private int age;

public int Age
{
    get { return age; }
    set
    {
        if (value >= 0)
            age = value;
    }
}
```

The property checks the value before changing the field.
