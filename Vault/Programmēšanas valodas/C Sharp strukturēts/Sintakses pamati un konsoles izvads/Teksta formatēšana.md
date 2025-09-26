___

**Datums:** 2025-08-04   
**Laiks:** 17:48 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

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
Iepriekšēja lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Sintakses pamati un konsoles izvads/Skaitļu izmantošana tekstā|Skaitļu izmantošana tekstā]]
Nākama lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Sintakses pamati un konsoles izvads/Composite Formatting|Composite Formatting]]

___