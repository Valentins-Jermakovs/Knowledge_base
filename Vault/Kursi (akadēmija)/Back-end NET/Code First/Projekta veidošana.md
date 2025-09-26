___

**Datums:** 2025-09-20
**Laiks:** 15:24
❚ **Tagi:** #back-end #NET 

---
### Projekta veidošana

Šādi izskatās modeļi:

1. Movie.cs:

```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

// Šo vajag pieslēgt, lai varētu veidot tabulas - obligāts
using Microsoft.EntityFrameworkCore;

namespace CodeFirst.Models
{
    public class Movie
    {
        // Šis būs primārais atslēgas lauks
        public int MovieId { get; set; }
        // Pārējie lauki
        public string Title { get; set; }
        public string Genre { get; set; }
        public DateTime ReleaseDate { get; set; }
        public decimal Price { get; set; }
        // Navigācijas īpašība - saistība ar Characters klasi (viena uz daudziem)
        // Foreign key būs Characters klases MovieId lauks
        public ICollection<Characters> Characters { get; set; } = new List<Characters>();
    }
}
```

2. Characters.cs:

```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

using Microsoft.EntityFrameworkCore;

namespace CodeFirst.Models
{
    public class Characters
    {
        public int CharactersId { get; set; }
        public string Name { get; set; }
        public string Role { get; set; }
        public int MovieCount { get; set; }
        // Foreign key uz Movie klasi
        public int MovieId { get; set; }
        // Navigācijas īpašība uz Movie klasi
        public Movie Movie { get; set; }
    }
}
```

Navigācijas īpašības nepieciešamas, lai vienkārši izvilkt datus no tabulas. Sanāk, ka tādējādi mēs varam vienkāŗsi piekļūt pie `Foreign-key` objektiem.


```cs
// Ielādē filmu kopā ar tās varoņiem
var movie = context.Movies
                   .Include(m => m.Characters) // EF pats izdara JOIN
                   .First(m => m.MovieId == 1);

Console.WriteLine($"Filma: {movie.Title}");
foreach (var ch in movie.Characters)
{
    Console.WriteLine($" - {ch.Name} ({ch.Role})");
}

```

Šādi tas izskatās tabulās:

```
Movies
-------
MovieId (PK)
Title
Genre
ReleaseDate
Price

Characters
----------
CharactersId (PK)
Name
Role
MovieCount
MovieId (FK) ---> Movies.MovieId
```

Šādi izskatās `Context.cs` fails:

```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

// Šo vajag pieslēgt, lai varētu veidot tabulas - obligāts
using Microsoft.EntityFrameworkCore;
// Pieslēdzam modeļus - tabulas
using CodeFirst.Models;

namespace CodeFirst.Data
{
    public class Context : DbContext
    {

        // Šeit pieslēdzam modeļus - tabulas
        public DbSet<Movie> Movie { get; set; }
        public DbSet<Characters> Characters { get; set; }

        // Konstruuktors, kas pieņem DbContextOptions un nodod to pamatklasei
        public Context(DbContextOptions<Context> options) 
            : base(options) 
        {
        }

        // Noklusētais konstruktors
        public Context() 
        {
        }

        // Šeit konfigurējam savienojumu ar SQL Server datubāzi
        protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder)
        {
            // Pārbaudām, vai opcijas jau nav konfigurētas
            if (!optionsBuilder.IsConfigured)
            {
                optionsBuilder.UseSqlServer("Server=LOQ;Database=MovieDB;Trusted_Connection=True;TrustServerCertificate=true");
            }
            // Izsaucam pamatklases metodi
            base.OnConfiguring(optionsBuilder);
        }


    }
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Mapju veidošana]]
Nākama lapa >>> [[Migrācijas]]

---