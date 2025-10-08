___

**Datums:** 2025-10-08
**Laiks:** 14:46
❚ **Tagi:** #back-end #NET 

---
# LINQ

`LINQ` tā ir vienkāršo vaicājumu valoda, kas konvertē `C#` kodu `SQL` vai citu valodu pieprasījumos.

Obligāti, lai `LINQ` vaicājumi darbotos, nepieciešams importēt bibliotēku - `using System.Linq;`.

Šādi izskatās vienkāršs vaicājums, kas pēc savas struktūras līdzīgs `SQL`:

```cs
// Veidojam kontekstu
var context = new Context();

// Veicam pieprasījumu
var query = 
	// Atlasam datus no tabulas
	from movie in context.Movies
	// Filtrējam pēc nosaukuma
	where movie.Title.Contains("Mat")
	// Attēlojam datus - ierakstam
	select movie;
	
// Cikls, kas izvada datus
foreach (var movie in query)
{
	Console.WriteLine($"{movie.Title}");
}
```

Šādi izskatās paplašinātais pieprasījuma variants:

```cs
// Veidojam kontekstu
var context = new Context();

// Veicam pieprasījumu
var query = context.Movies
	.where(m => m.Title.Contains("Mat"))
	.ToList();

// Cikls, kas izvada datus
foreach (var movie in query)
{
	Console.WriteLine($"{movie.Title}");
}
```

`LINQ` sintakses struktūra:

1. Ierakstam, no kurienes ņemt  datus;
2. `where` - ierobežojam, filtrējam datus;
3. (opcionāli) kārtojam datus;
4. (opcionāli) grupējam datus;
5. Attēlojam datus `select`.

## LINQ sintakse

**LINQ darbības un piemēri:**

![[Pasted image 20251008145932.png]]

**Apvienošana**

![[Pasted image 20251008150001.png]]
![[Pasted image 20251008150043.png]]

## LINQ sintakse (paplašinātais pieraksts)

**LINQ darbības un piemēri:**

![[Pasted image 20251008150210.png]]
![[Pasted image 20251008150252.png]]

**Apvienošana:**

![[Pasted image 20251008150321.png]]
![[Pasted image 20251008150350.png]]

## Koda piemēri

### Filtrēšana & Projekcija

Šeit tiek filtrēti uz izvadīt dati.

**LINQ pamata sintakse:**

```cs
var recentSciFiQ = 
    (from m in context.Movies
     where m.Genre == "Sci-Fi" && m.ReleaseDate >= new DateTime(2010,1,1)
     select new { m.Id, m.Title, m.ReleaseDate })
    .ToList();
```

Kas šeit notiek:

1. `from m in context.Movies` - izvelkam datus no tabulas `Movies` un saglabājam to `m`;
2. `where m.Genre == "Sci-Fi"` - iegūstam tikai tos datus, kas atbilst filtram;
3. `&& m.ReleaseDate >= new DateTime(2010,1,1)` - otrs filtrs;
4. `select new { m.Id, m.Title, m.ReleaseDate }` - izveidojam objektu tikai ar norādītiem laukiem;
5. `.ToList()` - konvertējam iegūstos sdatus sarakstā.

Rezultātā iegūstam šādu objektu:

```
[
  { "Id": 1, "Title": "Inception", "ReleaseDate": "2010-07-16" },
  { "Id": 2, "Title": "Interstellar", "ReleaseDate": "2014-11-07" },
  { "Id": 3, "Title": "Dune", "ReleaseDate": "2021-10-22" }
]
```

**Paplašināta sintakse:**

```cs
var recentSciFi = context.Movies
	.Where(m => m.Genre == "Sci-Fi" && m.ReleaseDate >= new DateTime(2010,1,1))
	.Select(m => new { m.Id, m.Title, m.ReleaseDate })
	.ToList();
```

### Eksistence: Any() un All()

`Any()` pārbauda vai ir vismaz viena vērtība, kas atbilst nosacījuma.
`All()` pārbauda, vai visas vērtības atbilst nosacījumam.

Abas metodes atgriež `true` bai `false`, atkarībā no rezultāta.

**LINQ pamata sintakse:**

Atgriež filmu sarakstu, kur ir vismaz 1 varonis.

```cs
var withChars = 
	from m in context.Movies
	where m.Characters.Any()
	select new { m.Id, m.Title }).ToList();
```

**Paplašināta sintakse:**

```cs
// Šeit meklē vai ir vismaz 1 filma ar aktieri visā DB
bool hasAnyCharacters = context.Movies.Any(m => m.Characters.Any());
// Šeit All() saņem atbilžu sarakstu no Any()
// Ja ir kaut viena filma DB bez aktiera, All()
// atgriezīs false
bool allHaveCharacters = context.Movies.All(m => m.Characters.Any());
```

### Iekļaušana: Include / ThenInclude

**Metodes sintakse (Include):**

```cs
var moviesWithChars = context.Movies
    .Include(m => m.Characters)
    .AsNoTracking()
    .ToList();
```

Kas šeit notiek:

1. `context.Movies` iegūst visas filmas no tabulas `Movies`;
2. `.Include(m => m.Characters)` liek ielādēt visus ar filmām saistītos varoņus;
3. `.AsNoTracking()` lai vaicājums darbotos ātrāk;
4. `.ToList()` konvertē datus sarakstā.

Rezultāta tiek iegūts filmu saraksts, kur katrai filmai esot piesaistīts savs varoņu saraksts.

```cs
foreach (var m in moviesWithChars)
{
    Console.WriteLine(m.Title);
    foreach (var c in m.Characters)
        Console.WriteLine($" - {c.Name}");
}
```

**Vaicājumu sintakse:**

```cs
var moviesDto = (
    from m in context.Movies
    select new { 
        m.Title, 
        Characters = m.Characters.Select(c => c.Name) 
    }
)
.AsNoTracking()
.ToList();
```

Kas šeit notiek:

1. `context.Movies` iegūst visas filmas no tabulas `Movies`;
2. `select new { ... }` - izveidojam atsevišķu objektu, kurā ierakstīsim vaicājuma rezultātus;
3. `Characters = m.Characters.Select(c => c.Name)` ņemam tikai varoņu vārdus no tabulas `Characters`;
4. `.AsNoTracking()` lai vaicājums darbotos ātrāk;
5. `.ToList()` konvertē datus sarakstā.

Rezultātā iegūstam šādu objektu:

```
[
  { "Title": "Matrix", "Characters": ["Neo", "Trinity"] },
  { "Title": "Avatar", "Characters": ["Jake"] }
]
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[GitHub]]
Nākama lapa >>> [[šablons]]

---