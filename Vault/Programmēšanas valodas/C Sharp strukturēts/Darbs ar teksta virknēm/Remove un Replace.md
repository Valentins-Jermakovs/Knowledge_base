___

**Datums:** 2025-08-04   
**Laiks:** 18:47 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

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

Lai aizvietot konkrētus simbolus ar kādiem citiem simboliem.

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
Iepriekšēja lapa >>> [[IndexOf un LastIndex, IndexOfAny]]
Nākama lapa >>> [[Navigācija - C Sharp strukturēts]]

___