___

**Datums:** 2025-08-04   
**Laiks:** 18:57 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Metodes

`C#` valodā pastāv vairākas metodes darbam ar masīviem.

#### Masīva garuma noteikšana

Lai uzzināt, kāds ir masīva garums, izmanto īpašību `Length`:

```csharp
int[] arr = {1, 2, 3, 4, 5, 65, 7, 21, 90};

Console.WriteLine($"Masīva garums ir >>> {arr.Length}");
// Masīva garums ir >>> 9
```
#### Metodes `Sort()` un `Reverse()`

```csharp
string[] pallets = { "B14", "A11", "B12", "A13" };

Console.WriteLine("Sorted...");
Array.Sort(pallets); // Kārto masīvu
foreach (var pallet in pallets)
{
    Console.WriteLine($"-- {pallet}");
}

Console.WriteLine("");
Console.WriteLine("Reversed...");
Array.Reverse(pallets); // Apgriež masīvu
foreach (var pallet in pallets)
{
    Console.WriteLine($"-- {pallet}");
}
```

#### Metode `Clear()`

Šī metode ļauj *attīrīt* masīvu. Patiesību sakot, visas vērtības vienkārši tiks aizvietots `null` vai `0` atkarībā no datu tipa.

```csharp
string[] pallets = { "B14", "A11", "B12", "A13" };
Console.WriteLine("");

Array.Clear(pallets, 0, 2);
Console.WriteLine($"Clearing 2 ... count: {pallets.Length}");
foreach (var pallet in pallets)
{
    Console.WriteLine($"-- {pallet}");
}

// Clearing 2 ... count: 4
// -- 
// -- 
// -- B12
// -- A13
```

#### Metode `Resize()`

Šī metode ļauj paplašināt masīvu, pievienot papildus vietu jauniem elementiem.

```csharp
string[] pallets =  {"B14", "A11", "B12", "A13"};
Console.WriteLine("");

Array.Clear(pallets, 0, 2);
Console.WriteLine($"Clearing 2 ... count: {pallets.Length}");
foreach (var pallet in pallets)
{
    Console.WriteLine($"-- {pallet}");
}

Console.WriteLine("");
Array.Resize(ref pallets, 6); // Elementu skaits tagad ir 6
Console.WriteLine($"Resizing 6 ... count: {pallets.Length}");

pallets[4] = "C01"; // 5. elements
pallets[5] = "C02"; // 6. elements

foreach (var pallet in pallets)
{
    Console.WriteLine($"-- {pallet}");
}

// Clearing 2 ... count: 4
// -- 
// -- 
// -- B12
// -- A13

// Resizing 6 ... count: 6
// -- 
// -- 
// -- B12
// -- A13
// -- C01
// -- C02
```

Tādējādi rodas iepēja izmantot metodi `Resize` ne tikai paplašināšanai, bet arī elementu dzēšanai.

```csharp
string[] pallets = { "B14", "A11", "B12", "A13" };
Console.WriteLine("");

Array.Clear(pallets, 0, 2);
Console.WriteLine($"Clearing 2 ... count: {pallets.Length}");
foreach (var pallet in pallets)
{
    Console.WriteLine($"-- {pallet}");
}

Console.WriteLine("");
Array.Resize(ref pallets, 6);
Console.WriteLine($"Resizing 6 ... count: {pallets.Length}");

pallets[4] = "C01";
pallets[5] = "C02";

foreach (var pallet in pallets)
{
    Console.WriteLine($"-- {pallet}");
}

Console.WriteLine("");
Array.Resize(ref pallets, 3); // Šeit samazina masīvu līdz 3 elementiem
Console.WriteLine($"Resizing 3 ... count: {pallets.Length}");

foreach (var pallet in pallets)
{
    Console.WriteLine($"-- {pallet}");
}
```

```
Clearing 2 ... count: 4
--
--
-- B12
-- A13

Resizing 6 ... count: 6
--
--
-- B12
-- A13
-- C01
-- C02

Resizing 3 ... count: 3
--
--
-- B12
```

#### Metode `ToCharArray()`

Šī metode ļauj pārveidot `string` tipa datus uz `char` (simbolu) masīvu.

```csharp
string value = "abc123";
char[] valueArray = value.ToCharArray();

Console.Write("Array [ ");
foreach (var letter in valueArray)
{
    Console.Write($"{letter} ");
}
Console.Write("]\n");

// Array [ a b c 1 2 3 ]
```

#### `char` masīva konvertācija uz `string`

```csharp
string value = "abc123";
char[] valueArray = value.ToCharArray();
Array.Reverse(valueArray); // Apgriež masīvu
string result = new string(valueArray); // Konvertē masīvu uz string
Console.WriteLine(result);

// 321cba
```
#### Metode `Join()`

Šī metode ļauj atdalīt elementus vienu no otra grafiski, piemēram ar `,`. Taču tas darbojas tikai, ja datus konvertē uz `string`.

```csharp
string value = "abc123";
char[] valueArray = value.ToCharArray();
Array.Reverse(valueArray);

string result = String.Join(",", valueArray); // Atdala elementus ar komatu
Console.WriteLine(result);
```

#### Metode `Split()`

Šī metode ļauj atdalīt vienu elementu no otra iterācijās, dalīt `string` uz apakš-`string`.
Piemēram, jā ir kāds vārds, to var sadalīt pa burtiem, simboliem. Bet, lai to izdarīt, jānorāda simbolu atdālītāju, bieži vien tas ir `,`.

```csharp
string value = "abc123";
char[] valueArray = value.ToCharArray();
Array.Reverse(valueArray);
// string result = new string(valueArray);
string result = String.Join(",", valueArray);
Console.WriteLine(result);

string[] items = result.Split(',');
foreach (string item in items)
{
    Console.WriteLine(item);
}

// 3,2,1,c,b,a
// 3
// 2
// 1
// c
// b
// a
```

---
### ⇄ Saistības

Avots >>> [Упражнение. Изучение Clear() и Resize() - Training \| Microsoft Learn](https://learn.microsoft.com/ru-ru/training/modules/csharp-arrays-operations/3-exercise-clear-resize)
Iepriekšēja lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Masīvi un kolekcijas/Masīvi 2D|Masīvi 2D]]
Nākama lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Masīvi un kolekcijas/Saraksti|Saraksti]]

___