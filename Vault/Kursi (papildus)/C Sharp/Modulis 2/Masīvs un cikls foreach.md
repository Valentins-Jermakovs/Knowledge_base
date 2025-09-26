___
**Datums:** 2025-07-06   
**Laiks:** 11:50 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Masīva deklarēšana

`C#` valodā pastāv 2 veidi, kā deklarēt masīvu un tā elementus.

Pirmais variants, ir ierezervēt atmiņu un katru elementu deklarēt atsevišķi:

```csharp
string[] fraudulentOrderIDs = new string[3]; // array with 3 elements [0], [1], [2]

fraudulentOrderIDs[0] = "A123"; // first element
fraudulentOrderIDs[1] = "B456"; // second element
fraudulentOrderIDs[2] = "C789"; // third element
```

Otrais variants, deklarēt masīvu ar visiem tā elementiem:

```csharp
string[] fraudulentOrderIDs = ["A123", "B456", "C789"];
```

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
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Modulis 2/Loģiskie operatori]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp/Modulis 2/Komentāri]]
___