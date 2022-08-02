c-sharp-8 introduced the concept of nullable and non-nullable reference types. Prior to c-sharp 8 reference times could be null but, you can now configure them to no longer allow the null value.

This comes in with .net 6 for the main poackages.

Options are:
Default: non-nullable reference types are not supported
Opt-In project, opt-out files: Enable at a project level and, for files which need the old behaviour, opt-out
Opt-In files: Only enable the feature for individual files

You can configure this at the project level:
```
<PropertyGroup> ... <Nullable>enable</Nullable> </PropertyGroup>
```

And on a per file level:
```
#nullable disable
```

Or for per file activation:
```
#nullable enable
```

With nullable reference types enabled, you use the same syntax as you would for variables. aka:

public string? Thing

---
[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

---
#dotnet #c-sharp-8 #dotnet-6