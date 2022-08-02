Finalizers are used for freeing up unmanaged resources ( likes/etc)

Syntax is:
~ClassName() {
	//dealoccate stuff here
}


However, this requires two tripes to the GC. It's recomended to also call the dispose ( provided by IDispose interface [[c-sharp common interfaces]])

Syntax for this looks like:
```
public class Animal : IDisposable
{
  public Animal()
  {
    // allocate unmanaged resource
  }
  ~Animal() // Finalizer
  {
    Dispose(false);
  }
  bool disposed = false; // have resources been released?
  public void Dispose()
  {
    Dispose(true);
    // tell garbage collector it does not need to call the finalizer
    GC.SuppressFinalize(this); 
  }
  protected virtual void Dispose(bool disposing)
  {
    if (disposed) return;
    // deallocate the *unmanaged* resource
    // ...   
    if (disposing)
    {
      // deallocate any other *managed* resources
      // ...
    }
    disposed = true;
  }
}

```

---

[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

---
#dotnet 