___
**Datums:** 2025-06-30   
**Laiks:** 12:16 
❚ **Tagi:** #SQL
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Vairāku kolonnu apakšvaicājumi
Līdz šim esam aplūkojuši tikai apakšvaicājumus, kas atgriež vienu kolonnu. Taču varam strādāt arī ar apakšvaicājumiem, kas atgriež vairākas kolonnas un vairākas rindas (atvasinātas tabulas).

```sql
SELECT * FROM Reservations
    WHERE (room_id, price) IN (SELECT id, price FROM Rooms);
```

```sql
SELECT * FROM Rooms
WHERE (has_tv, has_internet, has_kitchen, has_air_con) IN (SELECT has_tv, has_internet, has_kitchen, has_air_con FROM Rooms WHERE id=11)
```

Šajā piemērā tiek salīdzināti visu istabu kolonnas ar konkrēto istabu, kuras id = 11.

---
### ⇄ Saistības
Avots >>> [Многостолбцовые подзапросы — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/subquery-with-several-column)
Iepriekšēja lapa >>> [[Apakšvaicājumi ar vairākām rindām un vienu kolonnu]]
Nākama lapa >>> [[Korelēti apakšvaicājumi]]
___