Always important to check if something is null if something is nullable.

You can do this in a few ways:

```
if (thisCouldBeNull != null)
{
	Do a  thing
}
```


in c-sharp 7, the is combined with the ! can be used

```
if (!(thisCouldBeNull is null))
```


In c-sharp-9, the is not was introduced
```
if (thisCouldBeNull is not null)
```

If you are using a member of a variable which might be null, you can use a conditional

```
//This will assign null to y
int? y = something?.Length
```

If you want to check if null and use a different variable you can use ?? (null-coalescing operator)

```
int result = something?.Length ?? 3;
```

When handling parameters, it's good to check for null values. This is done by a simple if statement:

```
if (something == null)
{
	throw new ArgumentNullException(nameof(something))
}
```

---
[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

---
#dotnet #c-sharp-7 #c-sharp-9 