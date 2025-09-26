___

**Datums:** 2025-09-13
**Laiks:** 14:50
❚ **Tagi:** #back-end #NET 

---
### Tabulu ierakstu izvads

Par piemēru paņemsim vienu no tabulas failiem, šeit tā ir kalendāra notikumu tabula:

```cs
using System;
using System.Collections.Generic;

namespace MemoBackEnd.Models;

public partial class CalendarEvent
{
	// Mainīgo bloks
	// Tos var gan nolasīt, gan ierakstīt
    public int EventId { get; set; }

    public int UserId { get; set; }

    public string Title { get; set; } = null!;

    public string? Description { get; set; }

    public DateTime StartTime { get; set; }

    public DateTime EndTime { get; set; }

    public DateTime? CreatedAt { get; set; }

    public virtual User User { get; set; } = null!;

	// Metode, kas ļauj izvadīt tabulas ierakstu
    public string CalendarToStringData()
    {
        return $"EventID: {EventId}, UserID: {UserId}, Title: {Title}, StartTime: {StartTime}, EndTime: {EndTime}, CreatedAt: {CreatedAt}";
    }
}
```

Tā kā `C#` ir `OOP` valoda, mēs varam pašā klasē definēt publiski pieejamo metodi, kas atbilst par tabulas rindas izvadu.

Un jau tālāk `program.cs` fails, kur izpildās pati programma:

```cs
// Šī rinda ir obligāta, ja DB tabulas un DbContext faili ir izvietoti savos katalogos
using MemoBackEnd.Models;

// Saglabā visus DB datus
var context = new MemoDbContext(); 

// Šeit DB dati tiek izvilkti atbilstoši savām tabulām
// Jāpievērš uzmanība, kā tie tiek konvertēti sarakstos!
var users = context.Users.ToList();                      // User table
var passwords = context.UserPasswords.ToList();          // Password table
var calendarEvents = context.CalendarEvents.ToList();    // Calendar events table

// Cikli, kur notiek sarakstu lementu (tabulu rindu) izvads

// Līnija atdalītājs
string separator = new string('=', 50);
separator = "#" + separator + "#";
Console.WriteLine(separator);

// Pirmais cikls - Users tabula
foreach (var user in users)
{
    Console.WriteLine($"UserID: {user.UserId}, UserName: {user.UserName}, Email: {user.Email}, CreatedAt: {user.CreatedAt}");
}
Console.WriteLine(separator);

// Otrais cikls - Passwords tabula
foreach (var password in passwords)
{
    Console.WriteLine($"PasswordID: {password.PasswordId}, UserID: {password.UserId}, PasswordHash: {password.PasswordHash}, CreatedAt: {password.CreatedAt}");
}
Console.WriteLine(separator);

// Trešais cikls - CalendarEvents tabula
// Šeit var apskatīt augstāk rakstītas klases metodes pielietojumu,
// kas ļauj ērti izvadīt tabulas rindas datus.
foreach (var calendarEvent in calendarEvents)
{
    // CalendarTable function usage example
    Console.WriteLine(calendarEvent.CalendarToStringData());
}
Console.WriteLine(separator);
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[DB pieslēgšana pie projekta]]
Nākama lapa >>> [[Navigācija - Code first]]

---