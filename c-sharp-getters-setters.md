c-sharp supports pretty standard getter/setter formatting
```
  public string Origin  
    {  
        get        {            return $"{Name} was born on {HomePlanet}";  
        }  
    }  
    public string Greeting => $"{Name} says 'Hello!'";  
    public int Age => System.DateTime.Today.Year - DateofBirth.Year;  
    public string FavoriteIceCream { get; set; }  
  
    private string favoritePrimaryColor;  
  
    public string FavoritePrimaryColor  
    {  
        get  
        {  
            return favoritePrimaryColor;  
        }  
  
        set  
        {  
            switch (value.ToLower())  
            {  
                case "red":  
                case "green":  
                case "blue":  
                    favoritePrimaryColor = value;  
                    break;  
                default:  
                    throw new System.ArgumentException(  
                        $"{value} is not a primary color. " + "Choose from: red, green, blue");  
            }  
        }    }}
```
 
 ---
 [[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]
 
 ---
 
#dotnet 