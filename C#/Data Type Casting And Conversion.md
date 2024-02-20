## Widening Conversion
Attempting to convert a data type that could hold _less_ information to a data type that can hold _more_ information.
```cs
int myInt = 3;
decimal myDecimal = myInt;
```
Output:
```
int: 3
decimal: 3
```

## Narrowing Conversion
Attempting to convert a data type that can hold _more_ information to a data type that can hold _less_ information. You may lose precision when converting. You need to perform a **cast** when doing a narrowing conversion.
```cs
decimal myDecimal = 3.14m;
int myInt = (int)myDecimal;
```
Output:
```
decimal: 3.14
int: 3
```

## Performing Data Conversions
To perform data conversion, you can use one of several techniques:
- Use a helper method on the data type
```cs
// Using Parse()
string first = "5";
string second = "7";
int sum = int.Parse(first) + int.Parse(second);
// Output: 12
```
> [!info] Use `TryParse()` to avoid a format exception
> ```cs
> string value = "102";
> int result = 0;
> if (int.TryParse(value, out result))
> {
>    Console.WriteLine($"Measurement: {result}");
> }
> else
> {
>    Console.WriteLine("Unable to report the measurement.");
> }
> ```

- Use a helper method on the variable
```cs
// Using ToString()
int first = 5;
int second = 7;
string message = first.ToString() + second.ToString();
// Output: 57
```

- Use the `Convert` class methods
```cs
// Using Convert
string value1 = "5";
string value2 = "7";
int result = Convert.ToInt32(value1) * Convert.ToInt32(value2);
// Output: 35
```

> [!info] Casting truncates, converting rounds up