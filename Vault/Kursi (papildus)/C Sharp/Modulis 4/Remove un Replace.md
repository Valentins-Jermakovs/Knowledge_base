___
**Datums:** 2025-07-09   
**Laiks:** 15:33 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### `Remove()`

Lai izdzēst tekstu no konkrētas pozīcijas.

```csharp
string data = "12345John Smith          5000  3  ";
string updatedData = data.Remove(5, 20);
Console.WriteLine(updatedData);
```

```
123455000  3
```

#### `Replace()`

```csharp
string message = "This--is--ex-amp-le--da-ta";
message = message.Replace("--", " ");
message = message.Replace("-", "");
Console.WriteLine(message);
```

```
This is example data
```

---
### ⇄ Saistības
Avots >>> [Exercise - Use the Remove() and Replace() methods - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-modify-content/4-exercise-remove-replace)
Iepriekšēja lapa >>> [[IndexOf un LastIndex]]
Nākama lapa >>> [[Navigācija - C Sharp]]
___