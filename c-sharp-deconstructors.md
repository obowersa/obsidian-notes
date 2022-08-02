c sharp supports the concept of deconstructors.  This breaks up a 'thing' into seperate variables.

For example:
```
// deconstructors
public void Deconstruct(out string name, out DateTime dob)
{
  name = Name;
  dob = DateOfBirth;
}
public void Deconstruct(out string name, 
  out DateTime dob, out WondersOfTheAncientWorld fav)
{
  name = Name;
  dob = DateOfBirth;
  fav = FavoriteAncientWonder;
}
```

---
[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

---
#dotnet