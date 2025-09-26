 ___

**Datums:** 2025-08-04   
**Laiks:** 17:56 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Metodes formatēšanai

|Metode|Apraksts|Piemērs|
|---|---|---|
|`PadLeft(n)`|Pievieno tukšumus pa kreisi līdz `n` simboliem|`"Hello".PadLeft(10)` → `" Hello"`|
|`PadRight(n)`|Pievieno tukšumus pa labi līdz `n` simboliem|`"Hello".PadRight(10)` → `"Hello "`|
|`PadLeft(n, x)`|Pievieno simbolu `x` pa kreisi līdz `n` garumam|`"Pad".PadLeft(6, '-')` → `"---Pad"`|
|`PadRight(n, x)`|Pievieno simbolu `x` pa labi līdz `n` garumam|`"Pad".PadRight(6, '-')` → `"Pad---"`|

> Ja teksts jau ir garāks par `n`, tad nekas netiek mainīts.

```csharp
string input = "Pad this";

// Pieliek 4 tukšumus pa kreisi (kopā 12 simboli)
Console.WriteLine(input.PadLeft(12));

// Pieliek 4 tukšumus pa labi (kopā 12 simboli)
Console.WriteLine(input.PadRight(12));

// Ar simboliem '-'
Console.WriteLine(input.PadLeft(12, '-'));
Console.WriteLine(input.PadRight(12, '-'));
```

```
    Pad this
Pad this    
----Pad this
Pad this----
```

#### Neliels papildinājums

`C#` ļauj veidot teksta virknes ar noteiktu simbolu skaitu:

```cs
string separator = new string('=', 50);
```

---
### ⇄ Saistības

Avots >>> [Exercise - Discover padding and alignment - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-format-strings/4-exercise-string-methods-padding)
Iepriekšēja lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Sintakses pamati un konsoles izvads/String interpolation|String interpolation]]
Nākama lapa >>> [[Navigācija - C Sharp strukturēts]]

___