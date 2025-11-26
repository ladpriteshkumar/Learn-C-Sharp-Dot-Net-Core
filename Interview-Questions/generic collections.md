
 ## What is Generic in C#?
Generics in C# allow you to define classes, interfaces, methods, and data structures with a placeholder for the data type. Instead of writing separate implementations for each type, you write one generic definition that works with any type, while still maintaining type safety and performance.

 ### 🔑 Key Points to Mention
#### Definition:
Generics introduce type parameters (like `<T>`) that let you create reusable code components without sacrificing type safety.
#### Benefits:
- Type Safety: Errors are caught at compile time, no need for casting.
- Performance: Avoids boxing/unboxing for value types.
- Reusability: One implementation works for multiple types.
- Maintainability: Cleaner, more readable code.
#### Examples:
```csharp
// Generic Class
public class GenericBox<T>
{
    private T value;
    public void Add(T item) { value = item; }
    public T Get() { return value; }
}

// Usage
GenericBox<int> intBox = new GenericBox<int>();
intBox.Add(10);
Console.WriteLine(intBox.Get()); // Output: 10

GenericBox<string> strBox = new GenericBox<string>();
strBox.Add("Hello");
Console.WriteLine(strBox.Get()); // Output: Hello
```

 
 ## What are generic collections

 Generic collections in .NET are strongly‑typed data structures provided by the `System.Collections.Generic` namespace. Unlike non‑generic collections (like `ArrayList` or `Hashtable`), generic collections enforce type safety at compile time, which eliminates the need for boxing/unboxing and reduces runtime errors.



#### Definition:
Generic collections store elements of a specific type, defined using type parameters (e.g., List<T>). This ensures type safety and better performance.

#### Advantages:
- Type Safety: Compile‑time checking prevents invalid type insertions.
- Performance: No boxing/unboxing overhead for value types.
- Flexibility: Can work with any data type using generics.
- Code Reusability: One implementation works for multiple types.
#### Common Generic Collections:
- List<T> → Dynamic array, fast indexing.
- Dictionary<TKey, TValue> → Key/value pairs with fast lookups.
- Queue<T> → FIFO structure.
- Stack<T> → LIFO structure.
- HashSet<T> → Unique elements, optimized for set operations.
- SortedList<TKey, TValue> / SortedDictionary<TKey, TValue> → Maintain sorted order.
-
#### Example:
```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        List<string> names = new List<string>();
        names.Add("Alice");
        names.Add("Bob");

        foreach (var name in names)
        {
            Console.WriteLine(name); // Type-safe, no casting required
        }
    }
}
```
