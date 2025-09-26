___
**Datums:** 2025-06-27   
**Laiks:** 15:29 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Atkārtojuma izslēgšana
Lai izslēgt atkārtojumus no izvada, tiek izmantots operators `DISTINCT`.

```SQL
SELECT [DISTINCT] поля_таблиц FROM наименование_таблицы;
```

#### DISTINCT vairākām kolonnām
Lai izmantot operatoru `DISTINCT` priekš vairākām kolonnām, vienkārši norādi tās caur komatu.

```SQL
SELECT DISTINCT first_name, last_name FROM User;
```

---
### ⇄ Saistības
Avots >>> [Исключение дубликатов, DISTINCT — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/distinct-operator)
Iepriekšēja lapa >>> [[Funkciju izmantošana]]
Nākama lapa >>> [[Operators WHERE]]
___