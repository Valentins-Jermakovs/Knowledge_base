___

**Datums:** 2025-08-04   
**Laiks:** 18:38 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

---
### ⬢ Detalizēts apraksts
#### `foreach` cikls

`foreach` ļauj iterēt pa masīva elementiem:

```csharp
int[] inventory = [200, 450, 700, 175, 250];
int sum = 0;
int bin = 0;

foreach (int items in inventory)
{
    sum += items;
    bin++; // bin = bin + 1
    Console.WriteLine($"Bin {bin} = {items} items (Running total: {sum})");
}
Console.WriteLine($"We have {sum} items in invetory.");
```

#### Praktiskais piemērs

```csharp
string[] arr = new string[8];

arr[0] = "B123";
arr[1] = "C234";
arr[2] = "A345";
arr[3] = "C15";
arr[4] = "B177";
arr[5] = "G3003";
arr[6] = "C235";
arr[7] = "B179";

foreach (string item in arr)
{
    if (item.StartsWith("B"))
    {
        Console.WriteLine(item);
    }
}
// Output:
// B123
// B177
// B179
```

---
### ⇄ Saistības

Avots >>> [Module assessment - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-arrays/6-knowledge-check)
Iepriekšēja lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Konstrukcijas/while cikls|while cikls]]
Nākama lapa >>> [[Navigācija - C Sharp strukturēts]]

___