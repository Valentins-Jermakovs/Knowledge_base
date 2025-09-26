___
**Datums:** 2025-07-12   
**Laiks:** 11:34 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### `2D` masīvi

##### `2D` masīvu deklarēšana

```csharp
using System;

class Program
{
    static void Main()
    {
        // Taisnstūra masīvs (divdimensionāls, int[,])
        int[,] taisnstura1 = new int[3, 2]; // Deklarēšana ar izmēriem, bez inicializācijas
        int[,] taisnstura2 = { { 1, 2 }, { 3, 4 }, { 5, 6 } }; // Inicializācija deklarējot
        int[,] taisnstura3 = new int[,] { { 7, 8 }, { 9, 10 } }; // Ar norādītu tipu

        // Zobratu masīvs (masīvs no masīviem, int[][])
        int[][] zobrats1 = new int[3][]; // Tikai ārējais garums
        zobrats1[0] = new int[] { 1, 2 };
        zobrats1[1] = new int[] { 3, 4, 5 };
        zobrats1[2] = new int[] { 6 };

        int[][] zobrats2 = new int[][] {
            new int[] { 10, 11 },
            new int[] { 12 },
            new int[] { 13, 14, 15 }
        };

        int[][] zobrats3 = {
            new[] { 20, 21 },
            new[] { 22 },
            new[] { 23, 24, 25 }
        };
    }
}
```

|Masīva tips|Piemērs|Paskaidrojums|
|---|---|---|
|`int[,]`|`new int[3,2]`|Taisnstūra masīvs ar fiksētiem izmēriem|
|`int[][]`|`new int[3][]` un tad pa rindām|Zobratu masīvs – katrai rindai var būt atšķirīgs garums|

##### Iterācija pa `2D` masīviem

###### Iterācija pa taisnstūra masīvam

```csharp
// Taisnstūra masīvs (int[,])
        int[,] taisnstura = {
            { 1, 2, 3 },
            { 4, 5, 6 }
        };

        // Iterācija ar for ciklu
        for (int i = 0; i < taisnstura.GetLength(0); i++) // rindas
        {
            for (int j = 0; j < taisnstura.GetLength(1); j++) // kolonnas
            {
                Console.Write(taisnstura[i, j] + " ");
            }
            Console.WriteLine();
        }

        Console.WriteLine();

        // Iterācija ar foreach (piezīme: nevar tieši piekļūt rindai un kolonnai)
        foreach (int vērtība in taisnstura)
        {
            Console.Write(vērtība + " ");
        }
```

###### Iterācija pa zobrata masīvam

```csharp
// Zobratu masīvs (int[][])
        int[][] zobrats = {
            new[] { 10, 11 },
            new[] { 12 },
            new[] { 13, 14, 15 }
        };

        // Iterācija ar for ciklu
        for (int i = 0; i < zobrats.Length; i++)
        {
            for (int j = 0; j < zobrats[i].Length; j++)
            {
                Console.Write(zobrats[i][j] + " ");
            }
            Console.WriteLine();
        }

        Console.WriteLine();

        // Iterācija ar foreach
        foreach (int[] rinda in zobrats)
        {
            foreach (int vērtība in rinda)
            {
                Console.Write(vērtība + " ");
            }
            Console.WriteLine();
        }
```

---
### ⇄ Saistības
Avots >>> [Тип ссылки массива - C# reference \| Microsoft Learn](https://learn.microsoft.com/ru-ru/dotnet/csharp/language-reference/builtin-types/arrays#multidimensional-arrays)
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Papildus pētījumi/Masīvi 1D]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp/Papildus pētījumi/Saraksti|Saraksti]]
___