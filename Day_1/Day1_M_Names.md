**review1.cs**
```c#
//Avoid using bad names
int days; // elapsed time in days
```

**review2.cs**
```c#
// use meaningful names and avoid commenting simple logic
var employees = employeeService.getEmployeeList()
```

**review3.cs**
```c#
// avoid using hungarian notation,
// this was used back when IDEs weren't as intelligent and type inferencing // was not possible

int counter;
string fullName;
DateTime modifiedDate;
```

**review4.cs**
```c#
// remove noise from variable names
public bool IsShopOpen(string day, int amount)
{
    // some logic
}
```

**review5.cs**
```c#
// constants should be in uppercase? is this consider mixing
const int DAYS_IN_WEEK = 7;
const int DAYS_IN_MONTH = 30;

// variable names should be lowercase
var songs = new List<string> { 'Back In Black', 'Stairway to Heaven', 'Hey Jude' };
var artists = new List<string> { 'ACDC', 'Led Zeppelin', 'The Beatles' };

// Follow the same naming nomenclature - camelCase
bool EraseDatabase() { }
bool RestoreDatabase() { }

// Class names should be capitalized
class Animal { }
class Alpaca { }
```

**review6.cs**
```c#
public class Employee
{
    public Datetime workDate { get; set; } // get set Start Working Date
    public Datetime modTime { get; set; } // get set Modification Time
}
```

**review7.cs**
```c#
// follow camelCase notation 
var employeePhone;

public double CalculateSalary(int workingDays, int workingHours)
{
    // some logic
}
```
