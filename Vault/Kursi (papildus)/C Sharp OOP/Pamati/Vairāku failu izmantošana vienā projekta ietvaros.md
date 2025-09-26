___
**Datums:** 2025-07-13   
**Laiks:** 14:58 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Vairāku failu izmantošana vienā projekta ietvaros

`C#` ļauj veidot programmas struktūru no mapēm un failiem, lai viss darbotos korekti, tos vienkārši nepieciešams pieslēgt. Zemāk ir aprakstīti varianti.

##### 1. Bez `namespace` (iesācējiem, bet nav ieteicams lieliem projektiem)

Šeit galveinaiss ir `public`. Šis pieejas modifikātors ļauj izmantot klases un to metodes jebkur, visā projekta ietvaros. Neskatoties uz to, kā tie var atrasties dažādāš direktorijās un failos.

Piem., `Models/Person.cs`

```csharp
public class Persona
{
    string vards;
    public Persona(string vards) => this.vards = vards;
    public void Sveiciens() => Console.WriteLine($"Sveiki, {vards}!");
}
```

Un tagad šī klase tiks izmantota `main` failā, kas atrodas citā direktorijā.

```csharp
class Program
{
    static void Main()
    {
        Persona p = new Persona("Valentīns");
        p.Sveiciens();
    }
}
```

#### 2. Izmantot vienu `namespaces` priekš visas programmas

Tas vēl saucas globālais `namespace`.
Darbojas tāpat kā iepriekšēja mertode, bet šeit jau ir konkrētāka programmas struktūra.

```csharp
// Person.cs
namespace ManaApp
{
    public class Persona
    {
        string vards;
        public Persona(string vards) => this.vards = vards;
        public void Sveiciens() => Console.WriteLine($"Sveiki, {vards}!");
    }
}
// Program.cs
namespace ManaApp
{
    class Program
    {
        static void Main()
        {
            Persona p = new Persona("Valentīns");
            p.Sveiciens();
        }
    }
}
```

#### 3. Izmantot `namespaces` un apakš `namespace`

Atšķirība ar iepriekšējo, mēs veidojam globālo `namespace` un veidojam tam apakškategorijas, caur punktu.

Svarīgi! Nav obligāti veidot globālo `namespace`, vienkārši norādi caur punktu, kā piemēros. Kompilators pats izveidos globālo `namespace` un tā apakškategorijas.

```csharp
// Models/Persona.cs
namespace MyApp.Models
{
    public class Persona
    {
        public void Sveiciens() => Console.WriteLine("Sveiki!");
    }
}

// Program.cs
using MyApp.Models;

class Program
{
    static void Main()
    {
        var p = new Persona();
        p.Sveiciens();
    }
}
```

`MyApp.ViewModels.User` punktu skaits un dziļums nav ierobežots.

Projekta struktūras piemērs:

```
global (глобальное пространство имён)
│
└── ManaApp
    │
    ├── Models
    │    ├── Persona
    │    └── Dzivnieks
    │
    ├── Services
    │    └── AuthService
    │
    └── Controllers
         ├── HomeController
         └── AccountController
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp OOP/Pamati/Abstraktās klases]]

___