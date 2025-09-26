___
**Datums:** 2025-07-05   
**Laiks:** 14:33 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Skaitliskie datu tipi — īss pārskats

| Tips      | Apraksts                           | Baitu skaits | Piemērs               | Piezīmes                        |
| --------- | ---------------------------------- | ------------ | --------------------- | ------------------------------- |
| `int`     | Vesels skaitlis                    | 4 baiti      | `int a = 25;`         | Bez komatiem                    |
| `float`   | Daļskaitlis ar mazāku precizitāti  | 4 baiti      | `float b = 1.5f;`     | Jāliek `f` beigās               |
| `double`  | Daļskaitlis ar lielāku precizitāti | 8 baiti      | `double c = 3.14;`    | Noklusētais tips komatiem       |
| `decimal` | Precīzs daļskaitlis                | 16 baiti     | `decimal d = 99.99m;` | Jāliek `m` beigās, bieži naudai |

```csharp
using System;

class Program
{
    static void Main()
    {
        // Vesels skaitlis
        int vecums = 25;

        // Peldošais punkts ar mazāku precizitāti
        float augstums = 1.75f;

        // Peldošais punkts ar lielāku precizitāti
        double pi = 3.14159;

        // Precīzs decimālskaitlis (bieži lietots naudas aprēķinos)
        decimal cena = 19.99m;

        // Izvadām visus rezultātus
        Console.WriteLine("Vecums (int): " + vecums);
        Console.WriteLine("Augstums (float): " + augstums);
        Console.WriteLine("Pi (double): " + pi);
        Console.WriteLine("Cena (decimal): " + cena);
    }
}
```

#### Tipu pārveidošana

`C#` valodā var īslaicīgi pārveidot vienu datu tipu citā.

|Nosaukums|Sintakse|Apraksts|
|---|---|---|
|**Tiešā pārveidošana**|`(tipa_nosaukums)`|Piespiedu pārveidošana, var zaudēt precizitāti|
|**Netiešā pārveidošana**|Automātiski|Droša, ja nav iespējams datu zudums|
|**Convert metode**|`Convert.ToInt32()`|Apaļo vērtību, pārveido ar noteiktiem noteikumiem|

```csharp
int vesels = 10;
double daļskaitlis = vesels;        // Netiešā pārveidošana (int -> double)

double x = 5.9;
int y = (int)x;                      // Tiešā pārveidošana (rezultāts: 5)

decimal vidējāAtzīme = (decimal) totalPoints / creditHours;

int veselaDaļa = (int)vidējāAtzīme;
int pirmaCipars = (int)(vidējāAtzīme * 10) % 10;
int otraCipars  = (int)(vidējāAtzīme * 100) % 10;
```

#### Atšķirība starp `(int)` un `Convert.ToInt32()`

|Izteiksme|Rezultāts (ja x = 5.9)|
|---|---|
|`(int)x`|`5` (nogriež daļu)|
|`Convert.ToInt32(x)`|`6` (noapaļo)|

<mark style="background: #ADCCFFA6;">Tiešā pārveidošanā skaitlis netiek noapaļots ne uz augšu, ne uz leju. Skaitļi aiz komata tiek vienkārši atmesti.</mark>

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Matemātiskas operācijas]]
Nākama lapa >>> [[Noslēguma darbs]]
___