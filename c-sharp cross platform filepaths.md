When working with filepaths, make sure not to make assumptions about file seperatoes/etc.
Instead, use an array of strings and combine them using the path 


Also, check if it exists before hand.

```
var newFolder = Combine(GetFolderPath(SpecialFolder.Personal), "Code", "Chapter9", "NewFolder");
```

---
[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

---
#dotnet