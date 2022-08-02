Instead of hiding it's better to use overriding where possible. This relies on the base class providing an overridable method ( using the virtual keyword)

---

**Good Practice**: Many real-world APIs, for example, Microsoft's Entity Framework Core, Castle's DynamicProxy, and Episerver's content models, require the properties that you define in your classes to be marked as `virtual` so that they can be overridden. Carefully decide which of your method and property members should be marked as `virtual`.

---
Also a note on inheritence, constructors arent inherited so much be explicitly called using base()


---
[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

[[c-sharp inheritence and hiding methods]]

---
#dotnet