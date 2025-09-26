___

**Datums:** 2025-08-04   
**Laiks:** 18:16 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Datu konvertācija

|Metode|Apraksts|Piemērots|
|---|---|---|
|`(tipa)`|Nestingrā konvertācija (cast)|Skaitļi → Skaitļi|
|`.ToString()`|Skaitlis → Teksts|Izvadēm, ziņojumiem|
|`Parse()`|Teksts → Skaitlis|Kad pārliecināti par ievadi|
|`Convert` klase|Universāla un precīzākā konvertācija|Teksts ↔ Skaitļi ar pārbaudi|
#### 1. Nestingrā konvertācija `cast`

```csharp
decimal myDecimal = 3.14m;
int myInt = (int)myDecimal; // Zaudē daļu aiz komata

Console.WriteLine(myInt); // Rezultāts: 3
```

#### 2. Skaitlis uz tekstu `ToString()`

```csharp
int a = 5;
int b = 7;
string result = a.ToString() + b.ToString();

Console.WriteLine(result); // Rezultāts: "57"
```

#### 3. Teksts uz skaitli `Parse()`

```csharp
string x = "5";
string y = "7";
int sum = int.Parse(x) + int.Parse(y);

Console.WriteLine(sum); // Rezultāts: 12
```

#### 4. `Convert` klase - universāla metode

```csharp
string val1 = "5";
string val2 = "7";
int product = Convert.ToInt32(val1) * Convert.ToInt32(val2);

Console.WriteLine(product); // Rezultāts: 35
```

---
### ⇄ Saistības

Avots >>> [Exercise - Explore data type casting and conversion - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-convert-cast/2-exercise-data-type-conversion)
Iepriekšēja lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Mainīgie un datu tipi/Skaitliskie datu tipi - īss pārskats|Skaitliskie datu tipi - īss pārskats]]
Nākama lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Mainīgie un datu tipi/TryParse metode|TryParse metode]]

___