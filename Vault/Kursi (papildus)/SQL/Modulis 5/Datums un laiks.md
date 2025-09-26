___
**Datums:** 2025-07-01   
**Laiks:** 15:05 
❚ **Tagi:** #SQL
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Laika datu virknes attēlojums

| Tips        | Formāts pēc noklusējuma                                |
| ----------- | ------------------------------------------------------ |
| `DATE`      | `YYYY-MM-DD`                                           |
| `DATETIME`  | `YYYY-MM-DD hh:mm:ss`                                  |
| `TIMESTAMP` | `YYYY-MM-DD hh:mm:ss`                                  |
| `TIME`      | `hhh:mm:sss`                                           |
| `YEAR`      | `YYYY` - pilns formāts<br>`YY` vai `Y` saīsinātā forma |

Laika definēšanas\iestatīšanas piemēri:

```sql
SELECT  CAST("2022-06-16 16:37:23" AS DATETIME) AS datetime_1,
        CAST("2014/02/22 16*37*22" AS DATETIME) AS datetime_2,
        CAST("20220616163723" AS DATETIME) AS datetime_3,
        CAST("2021-02-12" AS DATE) AS date_1,
        CAST("160:23:13" AS TIME) AS time_1,
        CAST("89" AS YEAR) AS year
```

#### Reālā laika ģenerācija

Šim nolūkam izmanto 3 funkcijas:
- `CURDATE()`
- `CURTIME()`
- `NOW()`

#### Funkcijas laika datu izvilkšanai

| Funkcija | Apraksts               |
| -------- | ---------------------- |
| `YEAR`   | Atgriež gadu           |
| `MONTH`  | Atgriež mēnesi (1-12)  |
| `DAY`    | Atgriež dienu (1-31)   |
| `HOUR`   | Atgriež stundu (0-23)  |
| `MINUTE` | Atgriež minūtes (0-59) |
#### DATETIME un TIMESTAMP
`DATETIME` - neievēro laika joslu.
`TIMESTAMP` - ievēro laika joslu.

#### Laika zona

Laika zonas iestatīšana serverim, izmanto `UTC` formātu.

```sql
SET GLOBAL time_zone = '+03:00';    // глобально
SET time_zone = '+03:00';           // для текущего пользователя
SET @@session.time_zone = '+03:00'; // для текущей пользовательской сессии
```

---
### ⇄ Saistības
Avots >>> [Дата и время — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/work-with-datetime-data-type)
Iepriekšēja lapa >>> [[Skaitļu datu tips]]
Nākama lapa >>> [[Funkcija CAST]]
___