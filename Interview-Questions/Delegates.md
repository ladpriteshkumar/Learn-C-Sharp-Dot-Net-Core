
### What is Delegates
A delegate in C# is a type-safe object that represents a reference to a method with a specific signature and return type. In simple terms, it’s like a function pointer but safer and more powerful, because it ensures that the method you assign matches the expected parameters and return type

### 🔑 Key Characteristics of Delegates
- Type-safe function pointer: Ensures the method signature matches the delegate declaration.
- Encapsulation of methods: Can reference both static and instance methods.
- First-class object: Delegates can be stored in variables, passed as parameters, or returned from methods.
- Foundation of events: Events in C# are built on delegates, making them essential for event-driven programming.
- Supports flexible programming: Enables callbacks, anonymous methods, and lambda expressions.

#### 📘 Example
```csharp
// Declare a delegate type
public delegate void Notify(string message);

class Program
{
    static void Main()
    {
        // Assign a method to the delegate
        Notify notifier = ShowMessage;

        // Invoke the method via delegate
        notifier("Delegates are powerful!");
    }

    static void ShowMessage(string msg)
    {
        Console.WriteLine(msg);
    }
}
```

Here:
- Notify is a delegate type that can point to any method taking a string and returning void.
- ShowMessage is assigned to the delegate, and calling notifier("...") executes that method indirectly.




