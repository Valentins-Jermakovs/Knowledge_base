___

**Datums:** 2025-08-04   
**Laiks:** 19:11 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Kods

```csharp
// Variables
string? userInput;          // To allow Null in input
bool conversation = false;
bool flag = false;
int userValue = 0;

// do-while
Console.WriteLine("Enter an integer value between 5 and 10");
do
{
    userInput = Console.ReadLine();

    if (userInput != null)
    {
        conversation = int.TryParse(userInput, out userValue);

        if (conversation == true)
        {
            if ((userValue >= 5) || (userValue <= 10))
            {
                Console.WriteLine($"Your input value ({userValue}) has been accepted.");
                flag = true;
            }
            else
            {
                Console.WriteLine("Sorry, you entered an invalid number, please try again.");
            }
        }
        else
        {
            Console.WriteLine("Sorry, you entered an invalid number, please try again.");
        }
    }
    else
    {
        Console.WriteLine("Sorry, you entered an invalid number, please try again.");
    }
} while (flag == false);
```

```csharp
string users = "administrator|manager|user";
bool flag = false;

Console.WriteLine($"Enter your role name (Administrator, Manager, or User)");
do
{
    string? userInput = Console.ReadLine().Trim().ToLower();

    if (userInput != "")
    {
        if (users.Contains(userInput))
        {
            switch (userInput)
            {
                case "administrator":
                    Console.WriteLine("Your input value (Administrator) has been accepted.");
                    break;
                case "manager":
                    Console.WriteLine("Your input value (Manager) has been accepted.");
                    break;
                case "user":
                    Console.WriteLine("Your input value (User) has been accepted.");
                    break;
                default:
                    break;
            }
            flag = true;
        }
        else
        {
            Console.WriteLine($"The role name that you entered, \"{userInput}\" is not valid.\nEnter your role name (Administrator, Manager, or User)");
        }
    }
    else
    {
        Console.WriteLine("The role name that you entered, is not valid.\nEnter your role name (Administrator, Manager, or User)");
    }
} while (flag == false);
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - C Sharp strukturēts]]

___