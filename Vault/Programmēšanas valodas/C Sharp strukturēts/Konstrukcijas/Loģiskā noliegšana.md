___

**Datums:** 2025-08-04   
**Laiks:** 18:25 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

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

Avots >>> [Exercise - Evaluate an expression - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-evaluate-boolean-expressions/2-exercise-boolean-expressions)
Iepriekšēja lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Konstrukcijas/Loģiskie operatori|Loģiskie operatori]]
Nākama lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Konstrukcijas/Nosacījuma operators|Nosacījuma operators]]

___