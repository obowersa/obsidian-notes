A good tip seems to be to provide both a static and instance method within dotnet. This gives more flexibility

As an example:
```
using static System.Console;  
namespace PacktLibrary.Shared;  
  
public class Person  
{  
    public string? Name;  
    public DateTime DateOfBirth;  
    public List<Person> Children = new();  
  
  
    public static Person Procreate(Person p1, Person p2)  
    {  
        Person baby = new()  
        {  
            Name = $"Baby of {p1.Name} and {p2.Name}"  
        };  
        p1.Children.Add(baby);  
        p2.Children.Add(baby);  
        return baby;  
    }  
  
    public Person ProcreateWith(Person partner)  
    {  
        return Procreate(this, partner);  
    }  
    public void WriteToConsole()  
    {  
        WriteLine($"{Name} was born on a {DateOfBirth:dddd}.");  
    }  
}
```

---
[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

---
#dotnet