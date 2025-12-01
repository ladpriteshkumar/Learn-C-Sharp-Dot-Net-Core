### Check Even or Odd


```csharp
static bool IsEven(int n)
{
    // finding remainder of n
    int rem = n % 2;
    if (rem == 0)
    {
        return true;
    }
    else
    {
        return false;
    }
}

Console.WriteLine("10 is Even : "+ IsEven(10));  // true
Console.WriteLine("7 is Even : " + IsEven(7)); // false
```
