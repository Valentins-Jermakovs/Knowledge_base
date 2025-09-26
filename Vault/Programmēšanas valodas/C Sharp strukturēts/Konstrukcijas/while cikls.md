___

**Datums:** 2025-08-04   
**Laiks:** 18:36 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

---
### ⬢ Detalizēts apraksts
#### `do-while` un `while` cikli

Tas ir tas pats `while`, bet atšķirība tāda, kā bloks `do` izpildīsies vismaz 1 reizi.

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
Iepriekšēja lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Konstrukcijas/for cikls|for cikls]]
Nākama lapa >>> [[foreach cikls]]

___