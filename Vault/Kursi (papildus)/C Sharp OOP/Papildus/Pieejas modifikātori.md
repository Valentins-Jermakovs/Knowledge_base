___
**Datums:** 2025-07-13   
**Laiks:** 10:16 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Pieejas modifikatori

`C#` valodā pastāv šādi pieejas modifikatori:

- `public` - pieejams visām klasēm
- `private` - pieejams tikai vienas klases ietvaros
- `protected` - pieejams vienas klases ietvaros un tām klasēm, kas manto
- `internal` - tas ir kā `public`, bet darbojas tikai viena projekta ietvaros
- `protected internal` - darbojas viena projekta ietvaros un klass, kas manto
- `private protected` - darbojas viena projekta ietvaros un klasēs, kas manto

| Modifikators         | Pieejams tajā pašā klasē | Apakšklasēs (mantotās) | Tajā pašā montāžā (projektā) | Citās montāžās (projektos) |
| -------------------- | ------------------------ | ---------------------- | ---------------------------- | -------------------------- |
| `private`            | ✅                        | ❌                      | ❌                            | ❌                          |
| `protected`          | ✅                        | ✅                      | ❌                            | ✅ (ja mantots)             |
| `internal`           | ✅                        | ✅                      | ✅                            | ❌                          |
| `protected internal` | ✅                        | ✅                      | ✅                            | ✅ (ja mantots)             |
| `private protected`  | ✅                        | ✅                      | ✅                            | ❌                          |

#### `public`

```csharp
class Car
{
  public string model = "Mustang";
}

class Program
{
  static void Main(string[] args)
  {
    Car myObj = new Car();
    Console.WriteLine(myObj.model);
  }
}
```

#### `private`

```csharp
class Car
{
  private string model = "Mustang";

  static void Main(string[] args)
  {
    Car myObj = new Car();
    Console.WriteLine(myObj.model);
  }
}
```

#### `protected`

```csharp
class Animal
{
    protected void Breathe()
    {
        Console.WriteLine("Breathing...");
    }
}

class Dog : Animal
{
    public void Bark()
    {
        Breathe(); // можно вызвать, потому что Dog наследует Animal
        Console.WriteLine("Barking!");
    }
}
```

#### `internal`

```csharp
internal class Helper
{
    internal void DoSomething()
    {
        Console.WriteLine("Doing something...");
    }
}

// Можно вызвать в этом же проекте, но не из другого проекта/сборки
```

---
### ⇄ Saistības

Avots >>> [C# Access Modifiers](https://www.w3schools.com/cs/cs_access_modifiers.php)
Iepriekšēja lapa >>> [[Navigācija - C Sharp strukturēts]]

___