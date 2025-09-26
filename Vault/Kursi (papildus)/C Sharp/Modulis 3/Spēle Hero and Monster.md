___
**Datums:** 2025-07-07   
**Laiks:** 12:37 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Kods

```csharp
// Game players
int hero = 10;
int monster = 10;

// Attack logic
Random attack = new();
Console.WriteLine("==============================================");
Console.WriteLine("**********************GAME********************");
Console.WriteLine("==============================================");
// Game statement
while ((hero > 0) && (monster > 0))
{
    // First attack Hero -> Monster
    int heroAttack = attack.Next(1, 11);
    monster = monster - heroAttack;
    Console.WriteLine($"Damage to Monster [{heroAttack}]. Monster health [{monster}]");

    if (monster > 0)
    {
        int monsterAttack = attack.Next(1, 11);
        hero = hero - monsterAttack;
        Console.WriteLine($"Damage to Hero [{monsterAttack}]. Hero health [{hero}]");
    }
}
Console.WriteLine("==============================================");
// Game winner
if (hero > monster)
{
    Console.WriteLine("\t\tHero Win!");
}
else
{
    Console.WriteLine("\t\tMonster Win!");
}
Console.WriteLine("==============================================");
```

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Modulis 3/while cikls]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp/Modulis 3/Lietotāja ievada apstrāde]]
___