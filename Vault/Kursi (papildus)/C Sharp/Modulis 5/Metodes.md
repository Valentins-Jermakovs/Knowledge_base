___
**Datums:** 2025-07-10   
**Laiks:** 12:16 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Metodes sintakse

`C#` ļauj veidot savas metodes. Tam nevajag būt uzrakstītam obligāti pirms to izsaukšanas, var arī pēc.

```csharp
int[] a = {1,2,3,4,5};

Console.WriteLine("Contents of Array:");
PrintArray();

void PrintArray()
{
    foreach (int x in a)
    {
        Console.Write($"{x} ");
    }
    Console.WriteLine();
}
```

---
### ⇄ Saistības
Avots >>> [Understand the syntax of methods - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/write-first-c-sharp-method/2-understand-syntax-of-methods)
Iepriekšēja lapa >>> [[Navigācija - C Sharp]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp/Modulis 5/Metodes ar parametriem]]
___