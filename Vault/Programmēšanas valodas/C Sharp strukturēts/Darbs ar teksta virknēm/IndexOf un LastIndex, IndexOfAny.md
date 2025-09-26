___

**Datums:** 2025-08-04   
**Laiks:** 18:44 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

---
### ⬢ Detalizēts apraksts
#### ` IndexOf`

Šī metode atgriež pirmās sakritības indeksu.

#### `LastIndex`

Šī metode atgriež pēdējās sakritības indeksu.

```csharp
string message = "hello there!";

int first_h = message.IndexOf('h');
int last_h = message.LastIndexOf('h');

Console.WriteLine($"For the message: '{message}', the first 'h' is at position {first_h} and the last 'h' is at position {last_h}.");
```

```
For the message: 'hello there!', the first 'h' is at position 0 and the last 'h' is at position 7.
```

#### `IndexOfAny()`

Atgriež pirmo sakritību ar masīvu.

```csharp
string message = "Hello, world!";
char[] charsToFind = { 'a', 'e', 'i' };

int index = message.IndexOfAny(charsToFind);

Console.WriteLine($"Found '{message[index]}' in '{message}' at index: {index}.");
```

```
Found 'e' in 'Hello, world!' at index: 1.
```

---
### ⇄ Saistības

Avots >>> [Exercise - Use the string's IndexOf() and LastIndexOf() helper methods - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-modify-content/3-exercise-lastindexof-indexof)
Iepriekšēja lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Darbs ar teksta virknēm/IndexOf un Substring|IndexOf un Substring]]
Nākama lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Darbs ar teksta virknēm/Remove un Replace|Remove un Replace]]

___