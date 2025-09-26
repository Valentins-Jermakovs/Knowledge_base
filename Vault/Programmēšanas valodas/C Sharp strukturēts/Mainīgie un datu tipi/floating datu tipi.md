___

**Datums:** 2025-08-04   
**Laiks:** 18:11 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

---
### ⬢ Detalizēts apraksts
#### `floating` datu tipi

`C#` valodā ir 3 datu tipi ar komatu:

- `float` - skaitlis ar komatu
- `double` - precīzāks nekā `float`
- `decimal` - domāts ļoti precīzai skaitļošanai, izmanto finansēs

```csharp
Console.WriteLine("");
Console.WriteLine("Floating point types:");

Console.WriteLine($"float  : {float.MinValue} to {float.MaxValue} (with ~6-9 digits of precision)");
Console.WriteLine($"double : {double.MinValue} to {double.MaxValue} (with ~15-17 digits of precision)");
Console.WriteLine($"decimal: {decimal.MinValue} to {decimal.MaxValue} (with 28-29 digits of precision)");
```

```csharp
Floating point types:
float  : -3.402823E+38 to 3.402823E+38 (with ~6-9 digits of precision)
double : -1.79769313486232E+308 to 1.79769313486232E+308 (with ~15-17 digits of precision)
decimal: -79228162514264337593543950335 to 79228162514264337593543950335 (with 28-29 digits of precision)
```

---
### ⇄ Saistības

Avots >>> [Exercise - Discover floating-point types - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-choose-data-type/4-exercise-floating-point-types)
Iepriekšēja lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Mainīgie un datu tipi/int datu tips|int datu tips]]
Nākama lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Mainīgie un datu tipi/Skaitliskie datu tipi - īss pārskats|Skaitliskie datu tipi - īss pārskats]]

___