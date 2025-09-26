___
**Datums:** 2025-07-06   
**Laiks:** 19:17 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Nosacījuma operators

Nosacījuma operators `?`: novērtē `bool` izteiksmi un atgriež vienu no diviem rezultātiem atkarībā no tā, vai `bool` izteiksme tiek novērtēta kā `patiesa` vai `aplama`. Nosacījuma operatoru parasti sauc par trīskāršo nosacījuma operatoru.

```csharp
<evaluate this condition> ? <if condition is true, return this value> : <if condition is false, return this value>
```

```csharp
int saleAmount = 1001;
int discount = saleAmount > 1000 ? 100 : 50;
Console.WriteLine($"Discount: {discount}");
```

---
### ⇄ Saistības
Avots >>> [Exercise - Implement the conditional operator - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-evaluate-boolean-expressions/3-exercise-conditional-operator)
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Modulis 2/Loģiskā noliegšana]]
Nākama lapa >>> [[Monētas mešana]]
___