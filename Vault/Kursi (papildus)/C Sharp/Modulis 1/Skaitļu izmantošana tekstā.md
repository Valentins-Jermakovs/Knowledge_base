___
**Datums:** 2025-07-04   
**Laiks:** 16:44 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Skaitļi tekstā

Šeit skaitļi tiek konvertēti tekstā:

```csharp
string firstName = "Bob";
int widgetsSold = 7;
Console.WriteLine(firstName + " sold " + widgetsSold + 7 + " widgets.");
// Bob sold 77 widgets.
```

Šeit pirmkārt tiek veikta saskaitīšana un tikai tad konvertācija uz tekstu:

```csharp
string firstName = "Bob";
int widgetsSold = 7;
Console.WriteLine(firstName + " sold " + (widgetsSold + 7) + " widgets.");
// Bob sold 14 widgets.
```

---
### ⇄ Saistības
Avots >>> [Exercise - Perform addition with implicit data conversion - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-basic-operations/2-exercise-add-numbers)
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Modulis 1/Teksta interpolācija]]
Nākama lapa >>> [[Matemātiskas operācijas]]
___