**review1.cs**
```c#
/// The evil if
// remove the unnecessary if-else statements
// my approach is good for the short term but long term if we have to add more opening days 
// the developer will first read my code then add it to the condition 
public bool IsShopOpen(string day)
{
    if (!string.IsNullOrEmpty(day))
    {
        day = day.ToLower();
        if (day == "friday" || day == "saturday" || day == "sunday")
        {
            return true;
        }
    }
    return false;

}

// other approach
// this is a data driven approach, here the openingDays is a variable that storing the necessary information 
// this openingDays could later be stored in a database or file...
public bool IsShopOpen(string day)
{
    if (string.IsNullOrEmpty(day))
    {
        return false;

    }
    var openingDays = new[] { "friday", "saturday", "sunday" };
    return openingDays.Any(d => d == day.ToLower())
}
```

**review3.cs**
```c#
// my approach
public long Fibonacci(int n)
{
    if (n >= 50)
    {
        throw new System.Exception("Not supported");
    }

    if (n == 1 || n == 0)
    {
        return n;
    }


    return Fibonacci(n - 1) + Fibonacci(n - 2);
}

// avoid switch cases
```

**review4.cs**
```c#
var cities = new[] { "Austin", "New York", "San Francisco" };

for (var i = 0; i < cities.Count(); i++)
{
    var city = cities[i];
    DoStuff();
    DoSomeOtherStuff();

    // ...
    // ...
    // ...
    // Wait, what is `li` for again?
    Dispatch(city);
}
```

**review5.cs**
```c#
// magic numbers
// store the number as a constant or use enums  

const int ADMIN_ROLE = 8

if (userRole == ADMIN_ROLE) // Check if Admin 
{
    
}
```

**review6.cs**
```c#
// remove noise or reduntant words
public class Car
{
    public string make { get; set; }
    public string model { get; set; }
    public string color { get; set; }

    //...
}
```

**review7.cs**
```c#
// what the heck is this variable name: ymdstr

var currentDate = DateTime.UtcNow.ToString("MMMM dd, yyyy");
```

**review9.cs**
```c#
public void CreateMicrobrewery(string name = "Hipster Brew Co.")
{
    // ...
}
```
