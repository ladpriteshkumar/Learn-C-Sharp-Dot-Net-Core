## Differentiate between Array and ArrayList ?

In C#, the key difference between an Array and an ArrayList lies in size, type safety, and flexibility.
#### Array
- Fixed in size once created.
- Strongly typed — all elements must be of the same type.
- Provides better performance because there’s no boxing/unboxing overhead.
- Ideal when the number of elements is known and type safety is critical.
#### ArrayList
- Resizable — it can grow or shrink dynamically.
- Not strongly typed — it stores objects, so value types are boxed and unboxed.
- More flexible, but less efficient due to casting and boxing overhead.
- Useful when you  don’t know the size in advance.
  
👉 In modern C#, List<T> is generally preferred over ArrayList because it combines the flexibility of dynamic resizing with type safety and performance.

##### Example (to demonstrate in an interview)
```csharp
// Array
int[] numbers = new int[3] { 1, 2, 3 };

// ArrayList
using System.Collections;
ArrayList list = new ArrayList();
list.Add(1);
list.Add("Hello"); // Mixed types allowed
```



