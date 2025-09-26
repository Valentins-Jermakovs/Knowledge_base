___
**Datums:** 2025-07-05   
**Laiks:** 16:59 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Kods

```csharp
// Random dice = new Random(); izveido objektu ar klasi random (vecā koda versija)
Random dice = new(); // jaunā koda versija
int roll = dice.Next(1, 7); // izveidojam metienu
Console.WriteLine(roll);    // imitētajm kauliņa metienu un izvadam konsolē
```

Jaunā versija:

```csharp
Random dice = new();

int roll1 = dice.Next(); // no min līdz roll mx
int roll2 = dice.Next(101); // no 0 līdz 100
int roll3 = dice.Next(50, 101); // no 50 līdz 100

Console.WriteLine($"First roll: {roll1}");
Console.WriteLine($"Second roll: {roll2}");
Console.WriteLine($"Third roll: {roll3}");
```

Turpināt: [Exercise - Complete a challenge activity to discover and implement a method call - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-call-methods/5-exercise-challenge-call-method)

---
### ⇄ Saistības
Avots >>> [Exercise - Return values and parameters of methods - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-call-methods/4-exercise-return-values-input-parameters)
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Modulis 2/Projekta izveide]]
Nākama lapa >>> [[Programma, kas meklē lielāko vērtību no divām]]
___