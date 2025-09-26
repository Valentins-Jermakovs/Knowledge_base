___
**Datums:** 2025-07-01   
**Laiks:** 13:41 
❚ **Tagi:** #SQL
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Datu pievienošana
`INSERT` tiek izmantots, lai pievienotu tabulai jaunus ierakstus.

```sql
INSERT INTO имя_таблицы [(поле_таблицы, ...)]
VALUES (значение_поля_таблицы, ...)
| SELECT поле_таблицы, ... FROM имя_таблицы ...
```

Vērtības var ievietot, uzskaitot tās, izmantojot atslēgvārdu `VALUES`, norādot tās iekavās, atdalot tās ar komatiem, vai izmantojot `SELECT`.

Jauno ierakstu pievienošana iespējama 2 veidos:
- izmantojot sintaksi `INSERT INTO ... SELECT`
```sql
INSERT INTO Goods (good_id, good_name, type)
SELECT 20, 'Table', 2;
```
- izmantojot sintaksi `INSERT INTO ... VALUES (...)`
```sql
INSERT INTO Goods (good_id, good_name, type)
VALUES (20, 'Table', 2);
```

---
### ⇄ Saistības
Avots >>> [Добавление данных, оператор INSERT — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/operator-insert)
Iepriekšēja lapa >>> [[Navigācija - SQL]]
Nākama lapa >>> [[Datu atjaunošana, operators UPDATE]]
___