___

**Datums:** 2025-08-04   
**Laiks:** 18:31 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

---
### ⬢ Detalizēts apraksts
#### `for` cikls

`for` cikls domāts, lai iterēt pa vairāku dimensiju masīviem un mainīt masīva elementus.

```csharp
for (int i = 0; i < 10; i++) // 0 - 10
{
    Console.WriteLine(i);
}

for (int i = 10; i >= 0; i--) // 10 - 0
{
    Console.WriteLine(i);
}
```

Uzdevuma piemērs:

```csharp
for (int i = 1; i < 101; i++)
{
    if ((i % 3 == 0) && (i % 5 == 0))
    {
        Console.WriteLine($"{i} FizzBuzz");
    }

    else if (i % 3 == 0)
    {
        Console.WriteLine($"{i} Fizz");
    }

    else if (i % 5 == 0)
    {
        Console.WriteLine($"{i} Buzz");
    }

    else
    {
        Console.WriteLine(i);
    }
}
```

---
### ⇄ Saistības

Avots >>> [Exercise - Create and configure for iteration loops - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-for/2-exercise-for)
Iepriekšēja lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Konstrukcijas/Switch case konstrukcija|Switch case konstrukcija]]
Nākama lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Konstrukcijas/while cikls|while cikls]]

___