___
**Datums:** 2025-07-06   
**Laiks:** 19:15 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Loģiskā noliegšana

Termins "loģiskā noliegšana" attiecas uz unāro noliegšanas operatoru `!`. Daži cilvēki šo operatoru sauc par "not" operatoru. Kad operators `!` tiek ievietots pirms nosacījuma izteiksmes (vai jebkura koda, kas tiek novērtēts kā `true` vai `false`), tas piespiež kodu apgriezt operanda novērtēšanu. Pielietojot loģisko noliegšanu, novērtējums iegūst `true` , ja operands tiek novērtēts kā `false` , un `false` , ja operands tiek novērtēts kā `true` .

```csharp
// These two lines of code will create the same output
string pangram = "The quick brown fox jumps over the lazy dog.";

Console.WriteLine(pangram.Contains("fox") == false); //false
Console.WriteLine(!pangram.Contains("fox"));         //false
```

---
### ⇄ Saistības
Avots >>>[Exercise - Evaluate an expression - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-evaluate-boolean-expressions/2-exercise-boolean-expressions)
Iepriekšēja lapa >>> [[Programma, kas skaita studentu atzīmes]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp/Modulis 2/Nosacījuma operators]]
___