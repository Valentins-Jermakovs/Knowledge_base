___
**Datums:** 2025-07-04   
**Laiks:** 16:00 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Speciālo simbolu ekranēšana

Lai ekranēt speciālos simbolus, izmanto `\`. Piemēram, tekstā ievietot pēdiņas `\"`

- `\n` - jaunā rinda
- `\t` - tabulācija

`@` ļauj attēlot tekstu tā, kā tas ir rakstīts, bez speciālo simbolu izmantošanas.

```csharp
Console.WriteLine(@"    c:\source\repos    
        (this is where your code goes)");
```

![[Pasted image 20250704160234.png]]

`\u` - tiek izmantos, lai aprakstīt `unicode`  UTF-16 simbolus `string` teksta rindā.

```csharp
Console.Write("\u65e5"); //日
```

---
### ⇄ Saistības
Avots >>> [Exercise - Combine strings using character escape sequences - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-basic-formatting/2-exercise-character-escape-sequences)
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Modulis 1/Mainīgie|Mainīgie]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp/Modulis 1/Teksta apvienošana]]
___