___
**Datums:** 2025-06-30   
**Laiks:** 11:45 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Apakšvaicājumi ar vairākām rindām un vienu kolonnu
Ja apakšvaicājums atgriež **vairākas rindas ar vienu kolonnu**, tad, lai salīdzinātu šos datus, mēs varam izmantot trīs noderīgus operatorus: `ALL`, `ANY` un `IN`.
#### Operators ALL
Operators `ALL` pārbauda, vai **viena vērtība** ir **atbilstoša visām** vērtībām, ko atgriež apakšvaicājums. Šis nosacījums būs patiess (`TRUE`) **tikai tad**, ja **visi** salīdzinājumi dod pozitīvu rezultātu.

```sql
SELECT DISTINCT name FROM Users INNER JOIN Rooms
    ON Users.id = Rooms.owner_id
    WHERE Users.id <> ALL (
        SELECT DISTINCT user_id FROM Reservations
    )
```

Šajā piemērā tiek meklēti lietotāji, kuri iepriekš nav īrējuši istabas.

**Salīdzina ar visām vērtībām, atgriež ja pilnībā atbilst visiem nosacījumiem.**
#### Apakšvaicājums un IN operators
Operators `IN` pārbauda, vai konkrētā vērtība **ir sarakstā**, ko atgriež apakšvaicājums.

Šis vaicājums atgriež visus lietotājus, kuri **ir īpašnieki telpām, kuru cena ir vismaz 150 vienības**.

```sql
SELECT * FROM Users WHERE id IN (
    SELECT DISTINCT owner_id FROM Rooms WHERE price >= 150
)
```

#### Apakšvaicājums un ANY operators

Operators `ANY` pārbauda, vai viena vērtība **atbilst vismaz vienai** no apakšvaicājuma vērtībām.  
Rezultāts būs patiess (`TRUE`), ja vismaz **viena sakritība** tiks atrasta.

```sql
SELECT * FROM Users WHERE id = ANY (
    SELECT DISTINCT owner_id FROM Rooms WHERE price >= 150
)
```

Šis vaicājums arī atgriež lietotājus, kuri ir īpašnieki dārgām telpām, **bet pietiek ar vismaz vienu sakritību**, lai iekļūtu rezultātā.

**Salīdzina ar visām vērtībām, atgriež ja atbilst vismaz vienam nosacījumam\sakritībai.**

---
### ⇄ Saistības
Avots >>> [Подзапросы с несколькими строками и одним столбцом — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/subquery-with-one-column-several-row)
Iepriekšēja lapa >>> [[Vienas rindas vienas kolonnas apakšvaicājums]]
Nākama lapa >>> [[Vairāku kolonnu apakšvaicājumi]]
___