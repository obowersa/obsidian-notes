Records are introduced with c-sharp 9. They introduce the concept of an immutable object. Notably. They should not have any state ( fields or properties ) which change after initialisation.

To modify a record, you create a new record from an existing one with only the changed state being updated. This is a non-destructive mutation and uses the with keyword

Example:
```
public record ImmutableThing
{
	public int Something {get; init;}
	public string SomethingElse {get; init;}
}
```

```
ImmutableThing meep = new() {Something = 5, SomethingElse = 'HONK'}
ImmutableThing beep = meep with {SomethingElse = 'HONKHONK'}

```

records support constructors and deconstructors

---
c-sharp 10 introduced using records with structs

---
[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]
[[c-sharp-9-init]]	

---
#dotnet #c-sharp-9 #c-sharp-10