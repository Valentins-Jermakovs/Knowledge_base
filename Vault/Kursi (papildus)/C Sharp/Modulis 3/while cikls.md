___
**Datums:** 2025-07-07   
**Laiks:** 12:12 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### `do-while` cikls

Tas ir tas pats `while`, bet atšķirība tāda, kā tas izpildīsies vismaz 1 reizi.

```csharp
do
{
    // This code executes at least one time
} while (true);
```

```csharp
Random random = new Random();
int current = random.Next(1, 11);

/*
do
{
    current = random.Next(1, 11);
    Console.WriteLine(current);
} while (current != 7);
*/

while (current >= 3)
{
    Console.WriteLine(current);
    current = random.Next(1, 11);
}
Console.WriteLine($"Last number: {current}");
```

---
### ⇄ Saistības
Avots >>> [Add Looping Logic to your Code using the do-while and while Statements in C# - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-do-while/)
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Modulis 3/for cikls]]
Nākama lapa >>> [[Spēle Hero and Monster]]
___