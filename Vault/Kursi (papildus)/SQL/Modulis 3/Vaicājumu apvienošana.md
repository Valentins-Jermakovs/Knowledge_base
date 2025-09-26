___
**Datums:** 2025-06-30   
**Laiks:** 15:10 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Operators `UNION`
`SQL` vaicājumus var apvienot, tam izmanto operatoru `UNION`.

```sql
SELECT поля_таблиц FROM список_таблиц ...
UNION [ALL]
SELECT поля_таблиц FROM список_таблиц ... ;
```

Lai `UNION` darbotos pareizi, katra `SQL` vaicājuma iegūtajās tabulās ir jābūt vienādam kolonnu skaitam ar vienādu datu tipu un vienā un tajā pašā secībā.

#### Lietošanas piemērs
Piemēram, ir nepieciešams parādīt visu preču nosaukumus un visu ģimenes locekļu vārdus (ļoti nosacīts uzdevums). Tā kā datu tipi sakrīt, mēs to varam izdarīt.

```sql
SELECT DISTINCT Goods.good_name AS name FROM Goods
UNION
SELECT DISTINCT FamilyMembers.member_name AS name FROM FamilyMembers;
```

Rezultātā būs tabula, kur vienā kolonnā parādīs gan cilvēku vārdus, gan nopirkto preču nosaukumus.

```sql
SELECT Student.first_name, Student.middle_name, Student.last_name FROM Student
UNION
SELECT Teacher.first_name, Teacher.middle_name, Teacher.last_name FROM Teacher
```

---
### ⇄ Saistības
Avots >>> [Объединение запросов, оператор UNION — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/combining-queries)
Iepriekšēja lapa >>> [[Kopīga tabulas izteiksme, WITH priekšraksts]]
Nākama lapa >>> [[Loģika, CASE operators]]
___