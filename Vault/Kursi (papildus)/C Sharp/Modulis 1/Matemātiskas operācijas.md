___
**Datums:** 2025-07-04   
**Laiks:** 18:43 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Matemātiskas operācijas

`C#` valoda atbalsta šādas pamata matemātiskas operācijas:
- `+` saskaitīšana
- `-` atņemšana
- `*` reizināšana
- `/` dalīšana
- `%` atlikums / dalīšana pēc moduļa

```csharp
int sum = 7 + 5;
int difference = 7 - 5;
int product = 7 * 5;
int quotient = 7 / 5;

Console.WriteLine("Sum: " + sum);
Console.WriteLine("Difference: " + difference);
Console.WriteLine("Product: " + product);
Console.WriteLine("Quotient: " + quotient);

// Sum: 12
// Difference: 2
// Product: 35
// Quotient: 1
```

#### Inkrementi operatori

Standarta matemātiskām operācijām pastāv arī saīsinātā sintakse:

```csharp
int value = 1;

value = value + 1;
Console.WriteLine("First increment: " + value);

value += 1;
Console.WriteLine("Second increment: " + value);

value++;
Console.WriteLine("Third increment: " + value);

value = value - 1;
Console.WriteLine("First decrement: " + value);

value -= 1;
Console.WriteLine("Second decrement: " + value);

value--;
Console.WriteLine("Third decrement: " + value);
```

![[Pasted image 20250704184912.png]]

---
### ⇄ Saistības
Avots >>> [Exercise - Perform math operations - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-basic-operations/3-exercise-math-operators)
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Modulis 1/Skaitļu izmantošana tekstā]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp/Modulis 1/Skaitliskie datu tipi - īss pārskats]]
___