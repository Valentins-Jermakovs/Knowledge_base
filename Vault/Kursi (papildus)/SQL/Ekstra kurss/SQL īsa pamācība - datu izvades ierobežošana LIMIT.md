___

**Datums:** 2025-08-04   
**Laiks:** 11:16 

❚ **Tagi:** #SQL 
⌬ **Priekšmets:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Izvada ierobežošana

```sql
SELECT поля_выборки
FROM список_таблиц
LIMIT [количество_пропущенных_записей,] количество_записей_для_вывода;
```

```sql
SELECT * FROM Company LIMIT 2;
```

Šeit izvadīs tikai 2 ierakstus.

```sql
SELECT * FROM Company LIMIT 2, 3;
```

Šeit tiks izlaisti pirmie 2 ieraksti un izvadīs ierakstus no 3 līdz 5 ieskaitot.

<mark style="background: #FF5582A6;">Svarīgi! Operatoru LIMIT raksti pieprasījuma beigās!</mark>


---
### ⇄ Saistības

Iepriekšēja lapa >>> [[SQL īsa pamācība - konkrēto datu meklēšana WHERE]]
Nākama lapa >>> [[SQL īsa pamācība - datu šķirošana ORDER BY]]

___