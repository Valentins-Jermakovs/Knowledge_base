___

**Datums:** 2025-08-04   
**Laiks:** 19:01 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

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
Iepriekšēja lapa >>> [[Navigācija - C Sharp strukturēts]]
Nākama lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Metodes/Metodes ar parametriem|Metodes ar parametriem]]

___