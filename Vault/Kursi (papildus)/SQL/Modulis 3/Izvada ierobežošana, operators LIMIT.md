___
**Datums:** 2025-06-30   
**Laiks:** 10:11 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Izvada ierobežošana
```sql
SELECT поля_выборки
FROM список_таблиц
LIMIT [количество_пропущенных_записей,] количество_записей_для_вывода;
```

```sql
SELECT * FROM Company LIMIT 2, 3;
```

Šeit tiks izlaisti pirmie 2 ieraksti un izvadīs ierakstus no 3 līdz 5 ieskaitot.

<mark style="background: #FF5582A6;">Svarīgi! Operatoru LIMIT raksti pieprasījuma beigās!</mark>

---
### ⇄ Saistības
Avots >>> [Ограничение выборки, оператор LIMIT — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/limit)
Iepriekšēja lapa >>> [[Ārējs savienojums, OUTER JOIN]]
Nākama lapa >>> [[Apakšvaicājums]]
___