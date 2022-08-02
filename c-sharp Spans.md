You can use spans when dealing with arrays to look at a 'slice' of an array. This is a window into the original array and is more performant

The syntax for spans is

ReadOnlySpan<type>
	
You can use this with strings as well. So ReadOnlySpan<char> = nameAsSpan[^...something]

---
[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

---
#dotnet