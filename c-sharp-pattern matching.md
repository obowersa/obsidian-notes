Still need to fully grok this, but:

In c# 8, pattern matching looked like this :

```foreach (object passenger in passengers)  
{  
    decimal flightCost = passenger switch  
    {  
        FirstClassPassenger p when p.AirMiles > 35000 => 1500M,  
        FirstClassPassenger p when p.AirMiles > 15000 => 1750M,  
        FirstClassPassenger _ => 200M,  
        BusinessClassPassenger => 1000M,  
        CoachClassPassenger p when p.CarryOnKg < 10.0 => 500M,  
        CoachClassPassenger _ => 650M,  
        _ => 800M,  
    };  
    WriteLine($"Flight costs {flightCost:C} for {passenger}");  
}
```


Since c-sharp-9 and above, pattern matching now looks like this:
```
FirstClassPassenger p => p.AirMiles switch  
{  
    > 35000 => 1500M,  
    > 15000 => 1750M,  
    _ => 2000M  
},  
BusinessClassPassenger => 1000M,  
CoachClassPassenger p when p.CarryOnKg < 10.0 => 500M,  
CoachClassPassenger => 650M,  
_ => 800M,
```

OR
```
FirstClassPassenger {AirMiles: > 35000} => 1500M,  
FirstClassPassenger {AirMiles: > 15000} => 1750M,  
FirstClassPassenger => 2000M,  
BusinessClassPassenger => 1000M,  
CoachClassPassenger {CarryOnKg: < 10.0} => 500M,  
CoachClassPassenger => 650M,
```

---
[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

---
#dotnet #c-sharp-8 #c-sharp-10