___

**Datums:** 2025-09-20
**Laiks:** 15:53
❚ **Tagi:** #back-end #NET 

---
### Objekta (ieraksta) ierakstīšana DB

Šādi izskatās ieraksta ierakstīšana DB:

```cs
using Microsoft.EntityFrameworkCore;
using CodeFirst.Models;
using CodeFirst.Data;

// Pievienojam ierakstu tabulā Movie
using var context = new Context(); // Izveidojam kontekstu

/*
    Šeit tiek veidoti ieraksti 2 tabulās:
    1. Movie tabulā
    2. Characters tabulā
    Starp abām tabulām ir saistība - Foreign Key
    Vienai filmam var būt vairāki varoņi (Characters)
    Vienam varonim (Characters) var būt tikai viena filma (Movie)

    MovieID un CharactersID tiek ģenerēti automātiski,
    jo ir primārie atslēgas lauki
    Tos nav nepieciešams norādīt manuāli
 */

// Izveidojam jaunu Characters objektu
var character = new Characters
{
    // Piešķiram vērtības laukiem
    Name = "Dom Cobb",
    Role = "Main Character",
    MovieCount = 1,
    MovieId = 1 // Norādām saistīto MovieId
};

// Izveidojam jaunu Movie objektu
var movie = new Movie
{
    // Piešķiram vērtības laukiem
    Title = "Inception",
    Genre = "Science Fiction",
    ReleaseDate = new DateTime(2010, 7, 16),
    Price = 9.99M,
    // Pievienojam Characters objektu sarakstam
    Characters = new List<Characters> { character }

    /*
     * Šeit var arī izmantot lietotāja ievadu no konsoles,
     * lai iestatīt vērtības laukiem
     */
};

// Pievienojam Movie objektu kontekstam
context.Movie.Add(movie);
// Saglabājam izmaiņas datu bāzē
context.SaveChanges();

// Izvadām apstiprinājuma ziņu
Console.WriteLine("Dati veiksmīgi pievienoti datu bāzei!");
Console.WriteLine($"Movie: '{movie.Title}' added with ID: {movie.MovieId}.");
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Tabulas dzēšana]]
Nākama lapa >>> [[Navigācija - Code first]]

---