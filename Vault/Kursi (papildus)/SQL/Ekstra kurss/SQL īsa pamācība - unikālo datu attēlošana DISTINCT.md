___

**Datums:** 2025-08-04   
**Laiks:** 11:08 

❚ **Tagi:** #SQL 
⌬ **Priekšmets:**  `SQL`

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

Iepriekšēja lapa >>> [[SQL īsa pamācība - datu attēlošana SELECT]]
Nākama lapa >>> [[SQL īsa pamācība - konkrēto datu meklēšana WHERE]]

___