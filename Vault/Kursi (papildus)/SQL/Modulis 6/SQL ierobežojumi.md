___
**Datums:** 2025-07-02   
**Laiks:** 13:56 
❚ **Tagi:** #SQL
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Galvenie ierobežojumu veidi
| Ierobežojums  | Funkcija                                                |
| ------------- | ------------------------------------------------------- |
| `PRIMARY KEY` | Unikāls ieraksta ID, nevar būt `NULL`                   |
| `FOREIGN KEY` | Nodrošina sasaisti ar citu tabulu (atslēgas atbilstība) |
| `UNIQUE`      | Garantē unikālas vērtības kolonnā                       |
| `NOT NULL`    | Neļauj `NULL` vērtības                                  |
| `CHECK`       | Pārbauda vērtības pēc nosacījuma (piem. `price > 0`)    |
| `DEFAULT`     | Noklusētā vērtība, ja lietotājs neievada                |
Ierobežojumu pievienošana jaunai tabulai:

```sql
CREATE TABLE Users (
  id INT PRIMARY KEY,
  email VARCHAR(100) UNIQUE NOT NULL
);
```

Ierobežojumu pievienošana jau eksistējošai tabulai:

```sql
ALTER TABLE Users ADD CONSTRAINT uq_email UNIQUE (email);
ALTER TABLE Users DROP CONSTRAINT uq_email;
```

---
### ⇄ Saistības
Avots >>> [Ограничения столбцов (Constraints) — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/constraints)
Iepriekšēja lapa >>> [[Indeksi]]
Nākama lapa >>> [[Navigācija - SQL]]
___