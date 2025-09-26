___
**Datums:** 2025-07-06   
**Laiks:** 20:09 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Switch case

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
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Modulis 3/Saīsināta if operatora sintakses forma]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp/Modulis 3/for cikls]]
___