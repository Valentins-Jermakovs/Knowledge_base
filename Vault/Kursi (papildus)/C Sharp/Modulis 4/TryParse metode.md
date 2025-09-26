___
**Datums:** 2025-07-07   
**Laiks:** 17:40 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### `TryParse()` metode

Izmanto, lai **droši pārvērstu** tekstu uz skaitli **bez kļūdām**.  
Ja konvertācija izdodas - vērtība tiek ierakstīta `out` mainīgajā.

```csharp
string value = "123";
int result;

if (int.TryParse(value, out result))
    Console.WriteLine(result); // 123
else
    Console.WriteLine("Konvertācija neizdevās");
```

**`out result`** — šeit tiek ierakstīta konvertētā vērtība.  
Metode atgriež `true` vai `false`, lai pārbaudītu veiksmi, ko var saglabāt `bool` tipa mainīgā.

---
### ⇄ Saistības
Avots >>> [Exercise - Examine the TryParse() method - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-convert-cast/3-exercise-tryparse)
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Modulis 4/Datu konvertācija]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp/Modulis 4/Masīvu metodes]]
___