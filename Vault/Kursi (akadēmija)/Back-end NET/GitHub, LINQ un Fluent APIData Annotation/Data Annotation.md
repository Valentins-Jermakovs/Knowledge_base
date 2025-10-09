___

**Datums:** 2025-10-09
**Laiks:** 19:31
❚ **Tagi:** #back-end #NET 

---
# Data Annotation

![[Pasted image 20251009200436.png]]

Data Annotation ir atribūti, kurus uzliek tabulām (modeļos), lai veikt samēra vienkāršus noteikumus, attiecības.

Data Annotation tiek izmantots priekš vienkāršām lietām.

![[Pasted image 20251009194640.png]]


| Atribūts                   | Skaidrojums                                                              | Anotācija                                                                                          |
| -------------------------- | ------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------- |
| `[Table(“tbl_Course”)]`    | Pārdēvē tabulu datu bāzē, otrais parametrs pārdevē shēmu                 | `[Table(“tbl_Course”, Schema = “catalog”)]`                                                        |
| `[Column(“sName”)]`        | Pārdēvē kolonnas nosaukumu datu bāzē, otrais parametrs pārdevē datu tipu | `[Column(“sName”, TypeName = “varchar”)]`                                                          |
| `[Key]`                    | Norāda, ka lauks ir **primārais atslēga**                                |                                                                                                    |
| `[Required]`               | Lauks ir **obligāts** (NOT NULL)                                         |                                                                                                    |
| `[MaxLength(255)]`         | Norāda maksimāli pieļaujamu lauka garumu                                 |                                                                                                    |
| `[Index(IsUnique = true)]` | Atļauj ierakstīt laukā tikai unikālus datus                              |                                                                                                    |
| `[Foreignkey(“Author”)]`   | Iestata **FK** - Foreign Key                                             | `[Foreignkey(“Author”)]`<br>`Public int AuthorId {get; set;}`<br>`Public Author Author {get;set;}` |
Pēc anotāciju pieienošanas, modifikācijām, nepieciešams:

1. izveidot jauno migrāciju;
2. atjaunot datu bāzi.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[LINQ]]
Nākama lapa >>> [[Fluent API]]

---