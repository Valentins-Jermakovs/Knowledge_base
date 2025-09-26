___
**Datums:** 2025-07-01   
**Laiks:** 13:43

❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Datu dzēšana
Laiku pa laikam rodas uzdevums dzēst ierakstus no tabulas. Šim nolūkam `SQL` nodrošina `DELETE` un `TRUNCATE` operatorus, no kuriem pirmais variants ir visuniversālākais un drošākais.

#### Operators `DELETE`

```sql
DELETE FROM имя_таблицы
[WHERE условие_отбора_записей];
```

Ja trūkst `WHERE` ierakstu atlases nosacījuma, visi norādītajā tabulā esošie ieraksti tiks dzēsti.
To pašu darbību (visu ierakstu dzēšanu) var veikt arī, izmantojot operatoru `TRUNCATE`. Tas izdzēsīs tabulu un izveidos to no jauna - šī opcija ir daudz ātrāka nekā visu ierakstu dzēšana pa vienam (kā `DELETE` gadījumā), īpaši lielām tabulām.

#### Operators `TRUNCATE`

```sql
TRUNCATE TABLE имя_таблицы;
```

#### Datu dzēšana no daudztabulu vaicājumiem

Ja `DELETE` vaicājumā tiek izmantota `JOIN` funkcija, ir jānorāda, no kuras(-ām) tabulas(-ām) ieraksti ir jādzēš.

```sql
DELETE имя_таблицы_1 [, имя_таблицы_2] FROM
имя_таблицы_1 JOIN имя_таблицы_2
ON имя_таблицы_1.поле = имя_таблицы_2.поле
[WHERE условие_отбора_записей];
```

Izdzēš rezervāciju no istabām, kur `has_kitchen = false`

```sql
DELETE Reservations FROM
Reservations JOIN Rooms ON
Reservations.room_id = Rooms.id
WHERE Rooms.has_kitchen = false;
```

Izdzēš gan rezervāciju, gan istabu.

```sql
DELETE Reservations, Rooms FROM
Reservations JOIN Rooms ON
Reservations.room_id = Rooms.id
WHERE Rooms.has_kitchen = false;
```

---
### ⇄ Saistības
Avots >>> [Удаление данных, оператор DELETE — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/operator-delete)
Iepriekšēja lapa >>> [[Datu atjaunošana, operators UPDATE]]
Nākama lapa >>> [[SQL īsa pamācība - operators JOIN]]
___