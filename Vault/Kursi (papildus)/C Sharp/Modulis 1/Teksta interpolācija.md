___
**Datums:** 2025-07-04   
**Laiks:** 16:17 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Interpolācija

`C#` valodā darbā ar tekstu var izmantot mainīgos, ievietot tos tekstā. Lai to izdarīt, nepieciešams izmantot simbolu `$`.

```csharp
string firstName = "Bob";
string message = $"Hello {firstName}!";
Console.WriteLine(message);
// Hello Bob!

int version = 11;
string updateText = "Update to Windows";
string message = $"{updateText} {version}";
Console.WriteLine(message);
// Update to Windows 11

string projectName = "First-Project";
Console.WriteLine($@"C:\Output\{projectName}\Data");
// C:\Output\First-Project\Data
```

---
### ⇄ Saistības
Avots >>> [Exercise - Combine strings using string interpolation - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-basic-formatting/4-exercise-string-interpolation)
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Modulis 1/Teksta apvienošana]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp/Modulis 1/Skaitļu izmantošana tekstā]]
___