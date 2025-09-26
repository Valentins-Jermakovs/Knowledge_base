___
**Datums:** 2025-07-06   
**Laiks:** 10:14 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Loģiskie operatori

`C#` valodā pastāv šādi operatori:

- `if` - pārbaudīs to katru reizi
- `else if` - pārbauda, jā `if` nenostrāda
- `else` - nostrādās, kad iepriekš minētie operatori nenostrādāja

#### Salīdzināšanas operatori

`C#` valodā pastāv šādi salīdzināšanas operatori:

- `==` - vienāds
- `!=` - nav vienāds
- `>` - lielāks
- `<` - mazāks
- `>=` - lielāks vai vienāds
- `<=` - mazāks vai vienāds

`&&` - loģiskais **UN**, atgriež `True`, ja abi nosacījumi ir patiesi.
`||` - loģiskais **VAI**, atgriež `True`, ja viens no nosacījumiem ir patiess.

#### Koda piemērs no kursa

```csharp
Random dice = new();         // create dice

int roll1 = dice.Next(1, 7); // roll 1
int roll2 = dice.Next(1, 7); // roll 2
int roll3 = dice.Next(1, 7); // roll 3

int total = roll1 + roll2 + roll3; // sum of rolls

// output
Console.WriteLine($"Dice roll: [{roll1}] + [{roll2}] + [{roll3}] = |{total}|");

// if statements
if ((roll1 == roll2) || (roll2 == roll3) || (roll1 == roll3))
{
    if ((roll1 == roll2) && (roll2 == roll3))
    {
        Console.WriteLine("You rolled triples! +6 bonus to total!");
        total += 6;
    }
    else
    {
        Console.WriteLine("You rolled doubles! +2 bonus to total!");
        total += 2;
    }
    Console.WriteLine($"Your total including the bonus: {total}");
}

if (total >= 16)
{
    Console.WriteLine("You win a new car!");
}
else if (total >= 10)
{
    Console.WriteLine("You win a laptotp!");
}
else if (total == 7)
{
    Console.WriteLine("You win a trip for two!");
}
else
{
    Console.WriteLine("You win a kitten!");
}
```

```csharp
Random random = new();

int daysUntilExpiration = random.Next(12); // generate [0 - 11]
int discountPercentage = 0;

if (daysUntilExpiration == 0)
{
    Console.WriteLine("Your subscription has expired.");
}
else if (daysUntilExpiration == 1)
{
    Console.WriteLine("Your subscription expires within a day!\nRenew now and save 20%!");
    discountPercentage = 20;
}
else if (daysUntilExpiration <= 5)
{
    Console.WriteLine($"Your subscription expires in {daysUntilExpiration} days.\nRenew now and save 10%!");
}
else if (daysUntilExpiration <= 10)
{
    Console.WriteLine("Your subscription will expire soon. Renew now!");
    discountPercentage = 10;
}

if (discountPercentage > 0)
{
    Console.WriteLine($"Renew now and save {discountPercentage}%.");
}
```

---
### ⇄ Saistības
Avots >>> [Exercise - Create decision logic with if statements - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-if-elseif-else/2-exercise-if)
Iepriekšēja lapa >>> [[Programma, kas meklē lielāko vērtību no divām]]
Nākama lapa >>> [[Masīvs un cikls foreach]]
___