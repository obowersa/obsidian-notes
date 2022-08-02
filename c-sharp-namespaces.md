c sharp uses namespaces to group code. Think of it like modules/packages in python/golang.

With c# 10 language spec, there's a simplified namespace definition (this is called a filescoped namespace)

Instead of :
```
namespace Something 
{
	public class SomethingElse
	{
	}
}
```

You can instead use:
```
namespace Something;
public class SomethingElse
{
}
```

---
[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

---
#dotnet #c-sharp-10