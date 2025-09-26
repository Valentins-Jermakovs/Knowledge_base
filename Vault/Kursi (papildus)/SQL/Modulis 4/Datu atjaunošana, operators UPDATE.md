___
**Datums:** 2025-07-01   
**Laiks:** 13:42 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Datu atjaunošana
Lai rediģētu esošos ierakstus tabulās, ir `UPDATE`.

```sql
UPDATE имя_таблицы
SET поле_таблицы1 = значение_поля_таблицы1,
    поле_таблицыN = значение_поля_таблицыN
[WHERE условие_выборки]
```

```sql
UPDATE FamilyMembers
SET member_name = "Andie Anthony"
WHERE member_name = "Andie Quincey";
```

>Esiet uzmanīgi, atjauninot datus. Ja izlaidīsiet `WHERE`, tiks atjaunināti visi tabulas ieraksti.

---
### ⇄ Saistības
Avots >>> [Обновление данных, оператор UPDATE — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/operator-update)
Iepriekšēja lapa >>> [[Datu pievienošana, operators INSERT]]
Nākama lapa >>> [[Datu dzēšana, operators DELETE]]
___