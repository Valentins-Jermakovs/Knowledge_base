___
**Datums:** 2025-07-06   
**Laiks:** 19:58 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

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
Iepriekšēja lapa >>> [[Monētas mešana]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp/Modulis 3/Switch case konstrukcija]]
___