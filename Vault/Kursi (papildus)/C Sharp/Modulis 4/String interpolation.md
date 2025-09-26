___
**Datums:** 2025-07-09   
**Laiks:** 14:18 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### String interpolation

Kad teksta izvadei izmanto mainīgos, lai ērtāk formatēt izvadu.

```csharp
string first = "Hello";
string second = "World";
Console.WriteLine($"{first} {second}!");
Console.WriteLine($"{second} {first}!");
Console.WriteLine($"{first} {first} {first}!");

// Hello World!
// World Hello!
// Hello Hello Hello!
```

#### Izvada formatēšana

##### Valūta

Papildus ir `:C`, tas ļauj norādīt reģionā izmantoto valūtu. Tas nozīmē, kā katrā sistēmā tiks attēlots tas, kas ir raksturīgs iestatītam reģionam/valstij.

```csharp
decimal price = 123.45m;
int discount = 50;
Console.WriteLine($"Price: {price:C} (Save {discount:C})");
```

##### Skaitļi

Lai formatēt izvadu skaitļiem, attēlot ciparus aiz komata, izmanto `N`. Pie `N` var pievienot ciparu, kas norādīs, cik skaitļu parādīt aiz komata. Pēc standarta parāda 2 skaitļus. Sistēma pati saliks `,` vai `.`, atkarībā no iestatīta reģiona.

```csharp
decimal measurement = 123456.78912m;
Console.WriteLine($"Measurement: {measurement:N} units");

// Measurement: 123,456.79 units
```

##### Procenti

```csharp
decimal tax = .36785m;
Console.WriteLine($"Tax rate: {tax:P2}");

// Tax rate: 36.79%
```

Visu iepriekš minēto var kombinēt.

```csharp
decimal price = 67.55m;
decimal salePrice = 59.99m;

string yourDiscount = String.Format("You saved {0:C2} off the regular {1:C2} price. ", (price - salePrice), price);

yourDiscount += $"A discount of {((price - salePrice)/price):P2}!"; //inserted
Console.WriteLine(yourDiscount);
```

---
### ⇄ Saistības
Avots >>> [Exercise - Investigate string formatting basics - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-format-strings/2-string-formatting-basics)
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Modulis 4/Composite Formatting]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp/Modulis 4/String formatēšana PadLeft, PadRight un līdzināšana]]
___