___

**Datums:** 2025-08-04   
**Laiks:** 18:42 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

---
### ⬢ Detalizēts apraksts
#### `IndexOf` metode

Šī metode meklē meklējama simbola pozīciju tekstā un atgriež tā indeksu.
Atgriež `-1`, ja nespēj atrast simbolu.

```csharp
string message = "Find what is (inside the parentheses)";

int openingPosition = message.IndexOf('(');
int closingPosition = message.IndexOf(')');

Console.WriteLine(openingPosition);
Console.WriteLine(closingPosition);

// 13
// 36
```

#### `Substring()`

Šī metode ļauj atrast apakšrindu/apakštekstu.

```csharp
string message = "Find what is (inside the parentheses)";

int openingPosition = message.IndexOf('(');
int closingPosition = message.IndexOf(')');

openingPosition += 1;

int length = closingPosition - openingPosition;
Console.WriteLine(message.Substring(openingPosition, length));
```

```
inside the parentheses
```

---
### ⇄ Saistības

Avots >>> [Exercise - Use the string's IndexOf() and Substring() helper methods - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-modify-content/2-exercise-indexof-substring)
Iepriekšēja lapa >>> [[Navigācija - C Sharp strukturēts]]
Nākama lapa >>> [[IndexOf un LastIndex, IndexOfAny]]

___