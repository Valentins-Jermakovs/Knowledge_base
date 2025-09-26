___

**Datums:** 2025-08-04   
**Laiks:** 11:37 

❚ **Tagi:** #SQL 
⌬ **Priekšmets:**  `SQL`

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

>Esi uzmanīgs atjaunojot datus. Ja izlaidīsi `WHERE`, tiks atjaunināti visi tabulas ieraksti.

Labā prakse iesaka izmantot `PRIMARY_KEY`, kā filtru datu atjaunošanai, taču `WHERE` ļauj tev izmantot jebkuru kolonnu. Vienkārši esi uzmanīgs ar datu atjaunošanu.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[SQL īsa pamācība - jaunās kolonnas pievienošana esošai tabulai ALTER TABLE]]
Nākama lapa >>> [[SQL īsa pamācība - operators LIKE]]

___