
Common interfaces:
-	IComarable
	-	CompareTo(other)
	-	Allows for comparision between instances of a type, used for sorting and ordering
- IComparer
	- Compare(First, Second)
	- Allows comparision between two different types, used for ordering and sorting of a primary type
- IDisposable
	- Dispose()
	- Disposal method to release unamanaged resources instead of waiting for a finaliser	
- IFormatter
	- Serialize(stream,object), Deserialize(stream)
	- How you convert an object to and from a stream of bytes
- IFormattable
	- ToString(format, culture)
	- Culture-aware method to format something into a string representation
- IFormatProvider
	- GetFormat(type)
	- Format inputs based on the language and region

---
[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

---
#dotnet #c-sharp-interfaces