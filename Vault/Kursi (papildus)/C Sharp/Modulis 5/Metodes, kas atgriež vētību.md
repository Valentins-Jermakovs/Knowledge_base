___
**Datums:** 2025-07-10   
**Laiks:** 12:41 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Metodes, kas atgriež vērtību

`return` ļauj saglabāt funkcijas darbības rezultātu kādaā mainīgā.

```csharp
double usd = 23.73;
int vnd = UsdToVnd(usd);

Console.WriteLine($"${usd} USD = ${vnd} VND");
Console.WriteLine($"${vnd} VND = ${VndToUsd(vnd)} USD");

int UsdToVnd(double usd) 
{
    int rate = 23500;
    return (int) (rate * usd);
}

double VndToUsd(int vnd) 
{
    double rate = 23500;
    return vnd / rate;
}
```

---
### ⇄ Saistības
Avots >>> [Exercise - Return strings from methods - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/create-c-sharp-methods-return-values/4-exercise-create-methods-return-strings)
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Modulis 5/Metodes ar parametriem]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp/Modulis 5/Opcionāls parametrs]]
___