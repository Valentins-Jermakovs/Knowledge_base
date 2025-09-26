___

**Datums:** 2025-08-04   
**Laiks:** 18:28 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Kods

```csharp
int[] numbers = { 4, 8, 15, 16, 23, 42 };
int total = 0;
bool found = false;

foreach (int number in numbers)
{
    total += number;
    if (number == 42)
        found = true;
}

if (found) 
    Console.WriteLine("Set contains 42");

Console.WriteLine($"Total: {total}");
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Konstrukcijas/Nosacījuma operators|Nosacījuma operators]]
Nākama lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Konstrukcijas/Switch case konstrukcija|Switch case konstrukcija]]

___