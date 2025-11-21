### What is Global using ?
Global using in .NET (introduced in C# 10/.NET 6) is a feature that lets you declare a using directive once and make it available across your entire project, instead of repeating it at the top of every .cs file

🔑 Key Points
- Normal using directive: Allows you to reference types from a namespace without writing the full namespace path.
```csharp
using System.Text;
```
- Global using directive: When you add the global keyword, that namespace is automatically imported into all source files in the project.
```csharp
global using System.Text;
```
- Purpose:
- Reduces boilerplate code.
- Keeps files cleaner by avoiding repetitive using statements.
- Especially useful for common namespaces like System, System.Linq,




### 🔎 What a Namespace Is
- In .NET, a namespace is like a folder that groups related classes, structs, interfaces, and enums.
- Example: System.Text contains classes for text manipulation, like StringBuilder.
  
🧩 Without using

If you don’t import the namespace, you must write the full path every time:
```csharp
var sb = new System.Text.StringBuilder();
```

Here, you’re explicitly saying: “Go into the System.Text namespace and use the StringBuilder class.”

🧩 With using

If you add a using directive at the top of your file:
```csharp
using System.Text;

var sb = new StringBuilder();
```

Now you can reference `StringBuilder` directly, without writing `System.Text` each time.
The compiler already knows where to find it because of the using.

🌍 With Global Using

Instead of repeating `using System.Text;` in every file, you can declare it once as a global using:
```csharp
global using System.Text;
```

Placed in a file like `GlobalUsings.cs`, this makes StringBuilder available everywhere in your project automatically.


