___

**Datums:** 2025-08-04   
**Laiks:** 18:29 
❚ **Tagi:** #C_Sharp 

---
### ⬢ Detalizēts apraksts
#### `Switch...case` konstrukcija

```csharp
int employeeLevel = 100;
string employeeName = "John Smith";

string title = "";

switch (employeeLevel)
{
    case 100:   // Apvienots ar case 200
    case 200:
        title = "Senior Associate"; // Izpildās šis, jo case 100 un case 200 tagad ir apvienoti
        break;
    case 300:
        title = "Manager";
        break;
    case 400:
        title = "Senior Manager";
        break;
    default:
        title = "Associate";
        break;
}

Console.WriteLine($"{employeeName}, {title}");
```


---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Konstrukcijas/Saīsināta if operatora sintakses forma|Saīsināta if operatora sintakses forma]]
Nākama lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Konstrukcijas/for cikls|for cikls]]

___