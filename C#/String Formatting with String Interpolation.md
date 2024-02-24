## Formatting Currency

```cs
decimal price = 123.45m;
int discount = 50;
Console.WriteLine($"Price: {price:C} (Save {discount:C})");
```
Output:
```
Price: $123.45 (Save $50.00)
```

Currency formatting is dependent on the local computer setting for culture.

## Formatting Numbers

```cs
decimal measurement = 123456.78912m;
Console.WriteLine($"Measurement: {measurement:N} units");
```
Output:
```
Measurement: 123,456.79 units
```

By default, the `N` numeric format specifier displays only two digits after the decimal point. If you want to display more precision, you can do that by adding a number after the specifier.

```cs
decimal measurement = 123456.78912m;
Console.WriteLine($"Measurement: {measurement:N4} units");
```
Output:
```
Measurement: 123,456.7891 units
```

## Formatting Percentages
```cs
decimal tax = .36785m;
Console.WriteLine($"Tax rate: {tax:P2}");
```