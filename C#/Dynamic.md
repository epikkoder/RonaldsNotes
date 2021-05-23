## Type resolution
- Static languages: at compile-time
- Dynamic languages: at run-time

## History
- Started as a static language
- .NET 4 added the dynamic capability to improve interoperability with
  - COM (e.g. writing office applications)
  - Dynamic languages (IronPython)

Without dynamic, we'd have to use [[Reflection]]

```csharp
object obj = "Ronald";

// using Reflection
var methodInfo = obj.GetType().GetMethod("GetHashCode");
methodInfo.Invoke(null, null);

// using dynamic
dynamic excelObject = "Ronald";
excelObject.Optimize();
```

When you use dynamic variables to an expression, it will end up being dynamic as well.

```csharp
dynamic a = 10;
dynamic b = 5;
var c = a + b;
```
![[dynamic_expression.jpg]]

When coverting from dynamic to static types, if the run-time type of the dynamic object is implicity convertible to the target type, you don't need to cast it.

```csharp
int i = 5;
dynamic d = i;
long l = d;
```
![[dynamic_to_static.jpg]]