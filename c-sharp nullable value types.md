By default, value types like int/DateTime must always have a value. 

You can, however, force them to allow empty/null values. This is used a lot when interacting with databases/etc

Syntax for this is:
type? thing

so int? whattheFuck

You can use GetValueOrDefault() to either get the value or to print out the default for that type.

---
[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

---
#dotnet 