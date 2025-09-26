___
**Datums:** 2025-07-02   
**Laiks:** 12:17 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Datu bāzes izveide

```sql
CREATE DATABASE имя_базы_данных;
```

Operators `SHOW DATABASE` ļauj apskatīt izveidotas datu bāzes:

```sql
SHOW DATABASES;
```

Lūdzu, ņemiet vērā, ka operators `SHOW DATABASES` parāda ne tikai lietotāju datubāzes, bet arī sistēmas datubāzes: `information_schema`, `mysql`, `performance_schema`, `sys`.

#### Datu bāzes dzēšana

```sql
DROP DATABASE имя_базы_данных;
```

#### Konstrukcija `IF [NOT] EXIST`

Ja vēlamies izveidot datubāzi tikai tad, ja tā vēl neeksistē, tiek izmantota šāda sintakse:

```sql
CREATE DATABASE IF NOT EXIST имя_базы_данных;
```

Ja vēlamies dzēst datubāzi tikai tad, ja tāda pastāv, tiek izmantota šāda sintakse:

```sql
DROP DATABASE IF EXIST имя_базы_данных;
```

---
### ⇄ Saistības
Avots >>> [Создание и удаление баз данных — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/create-database)
Iepriekšēja lapa >>> [[Navigācija - SQL]]
Nākama lapa >>> [[Tabulas izveide un dzēšana]]
___