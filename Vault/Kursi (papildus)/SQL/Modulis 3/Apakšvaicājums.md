___
**Datums:** 2025-06-30   
**Laiks:** 10:22 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Apakšveicājums

> [!NOTE] Apakšvaicājums
> Apakšvaicājums ir vaicājums, kas tiek izmantots cita SQL vaicājuma ietvaros. Apakšvaicājums vienmēr ir ievietots iekavās un parasti tiek izpildīts pirms galvenā vaicājuma.

```sql
SELECT * FROM Reservations
    WHERE Reservations.room_id = (
        SELECT id FROM Rooms ORDER BY price DESC LIMIT 1
    )
```

Šajā pieprasījumā tiek izvadīta visdārgākā istaba īrēšanai.

---
### ⇄ Saistības
Avots >>> [Подзапросы — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/nested-sql-queries)
Iepriekšēja lapa >>> [[Izvada ierobežošana, operators LIMIT]]
Nākama lapa >>> [[Vienas rindas vienas kolonnas apakšvaicājums]]
___