# Common C# Mistakes and Debugging Checks

## 1. Accessing a private field from outside its class
**Problem:** Code outside a class tries to use a `private` field.

**Why:** `private` members are only accessible inside their containing type.

**Check:** Use a public property or method to provide controlled access.

## 2. Giving a constructor a return type
**Problem:** Writing `void Student()` as a constructor.

**Why:** A constructor has the same name as its class and no return type.

**Correct:**
```csharp
public Student()
{
}
```

## 3. Confusing `get` and `set`
- `get` reads/returns the property's value.
- `set` assigns a value.
- `value` inside `set` is the incoming value.

## 4. Calling an instance method like a static method
**Problem:** Calling `Student.Introduce()` when `Introduce` is not static.

**Why:** An instance method needs an object.

**Correct pattern:**
```csharp
Student student = new Student();
student.Introduce();
```

## 5. Calling a static method through an object
Use the type name for a static member:

```csharp
int answer = Calculator.Add(2, 3);
```

## 6. Using the wrong tuple element
- Unnamed tuple: use `Item1`, `Item2`, and so on.
- Named tuple: use the declared element names.

## Debugging checklist
1. Check spelling and capitalization.
2. Check that braces `{}` and parentheses `()` match.
3. Check semicolons at the ends of statements.
4. Check that variables are declared before use.
5. Check whether a member is `private`, `public`, `static`, or an instance member.
6. Read the first compiler error first; later errors may be caused by it.
