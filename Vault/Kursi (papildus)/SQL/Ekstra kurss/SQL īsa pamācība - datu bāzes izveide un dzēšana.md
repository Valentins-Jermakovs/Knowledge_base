___

**Datums:** 2025-08-04   
**Laiks:** 10:39 

❚ **Tagi:** #SQL 
⌬ **Priekšmets:**  `SQL`

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

Iepriekšēja lapa >>> [[SQL īsa pamācība - datu tipi]]
Nākama lapa >>> [[SQL īsa pamācība - tabulas izveide un dzēšana]]

___