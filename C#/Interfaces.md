If you have methods you're not ready to implement yet, it's common practice to throw a `NotImplementedException`.

```csharp
public void Return(int amount)
{
    throw new NotImplementedException();
}
```