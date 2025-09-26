___

**Datums:** 2025-09-13
**Laiks:** 12:31
❚ **Tagi:** #back-end #NET 

---
### Instrukcija Db pieslēgšanai pie projekta

Lai sadraudzēt datu bāzi un `.NET` projektu jāveic šādus soļus:

1. Izveidot pašu DB (kursa ietvaros tiek izmantots Microsoft SQL Server);
2. Izveidot jauno konsoles projektu;
3. Instalēt nepieciešamas paķetes;
4. Izpildīt komandu.

#### Jaunais konsoles projekts

![[Pasted image 20250913123400.png]]

Mums nepieciešams pats pirmais, kas atbalsta visas platformas. Obligāti, projekta izveides posmā izvēlies `.NET 9.0` versiju! *Aktuāls uz 2025. gada septembri.*

#### Paķešu instalācija

Lai sadraudzēt DB un kosnoles projektu, nepieciešamas šādas paķetes:

- `Microsoft.EntityFrameworkCore`
- `Microsoft.EntityFrameworkCore.Tools`
- `Microsoft.EntityFrameworkCore.SqlSer`

Lai tās sainstalēt dodies uz -> `Tools` -> `NuGet Package Manager` -> `Manage NuGet Packages for Solution...`. Laukā `Browse` ievadi iepriekš minētas paķetes un sainstalē tās vienu pēc otras. <mark style="background: #FFB86CA6;">Uzmanību! Visām 3 paķetēm jābūt ar vienādu versiju!</mark>

Projekta menedžerī jāparādas šādiem moduļiem:

![[Pasted image 20250913123843.png]]

#### Komandas izpilde

Pēdējais solis, lai pieslēgt DB pie paša projekta, ievadi `Package Manager Console` šādu komandu, pirms ievadīt, izlasi visu instrukciju!

```
Scaffold-DbContext "Server=DESKTOP-H8BOG5A;Database=database_first;Trusted_Connection=True;TrustServerCertificate=true;" Microsoft.EntityFrameworkCore.SqlServer
```

Šeit ir 2 vietas, kurām jāpievērš uzmanību:

- `Server=DESKTOP-H...` - šeit aiz `=` tev jāievada sava servera nosaukums, kuru tu vari apskatīt `Microsoft SQL Server Managment Studio`, kad veic pieslēgumu pie datu bāzes;
- `Database=database_first` - šeit aiz `=` tev jāievada savas datu bāzes nosaukumu.

Pēc visiem iepriekš aprakstītiem posmiem jāparādas līdzīgam kodam:

![[Pasted image 20250913124321.png]]
#### Komandas izpilde 2

Papildus pie šīs te komandas:

```
Scaffold-DbContext "Server=DESKTOP-H8BOG5A;Database=database_first;Trusted_Connection=True;TrustServerCertificate=true;" Microsoft.EntityFrameworkCore.SqlServer
```

Var pievienot `-OutputDir Models -ContextDir Data`, kur:

- `Models` - katalogs, kur tiks glabātas tabulas;
- `Data` - katalogs, kur tiks glabāts DB pieslēguma fails.

Pilnā variāntā komanda izskatās šādi:

```
Scaffold-DbContext "Server=DESKTOP-H8BOG5A;Database=database_first;Trusted_Connection=True;TrustServerCertificate=true;" Microsoft.EntityFrameworkCore.SqlServer -Output Models -ContextDir Data
```

<mark style="background: #ABF7F7A6;">Šis variants ir vairāk ieteicams, jo projekts tiek strukturēts uzreiz, tā izveides laikā.</mark>

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - back-end NET]]
Nākama lapa >>> [[Darbs ar DB, tabulu ierakstu izvads]]

---