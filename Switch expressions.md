In C# language 8.0, switch statements can be simplified using 'switch expressions'

They are used where all cases return the same value.

Example:
```
message = s switch
{
  FileStream writeableFile when s.CanWrite
    => "The stream is a file that I can write to.", 
  FileStream readOnlyFile
    => "The stream is a read-only file.", 
  MemoryStream ms
    => "The stream is a memory address.", 
  null
    => "The stream is null.",
  _
    => "The stream is some other type."
};
WriteLine(message);

```
The thing to note is the lack of a default (using underscore instead), the case of a break, and the use of =>

You can also use or statements with switches since dotnet 9. And other boolean expressions

---
[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

---
#dotnet #c-sharp-8 #c-sharp-9