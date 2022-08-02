Dotnet has a weird thing called 'checked'

Checked can be used for identifying buffer overflows by wrapping the code in a checked statement

So:

```
checked 
{
	// code goes here
}
```

It's disabled by default due to performance reasons

The opposite to this is unchecked. Which disables compile time checks for buffer overflows

---
[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

---

#dotnet