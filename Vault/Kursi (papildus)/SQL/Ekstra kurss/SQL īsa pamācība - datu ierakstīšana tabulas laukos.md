___

**Datums:** 2025-08-04   
**Laiks:** 10:56 

❚ **Tagi:** #SQL 
⌬ **Priekšmets:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Datu pievienošana

`INSERT` tiek izmantots, lai pievienotu tabulai jaunus ierakstus.

```sql
INSERT INTO имя_таблицы [(поле_таблицы, ...)]
VALUES (значение_поля_таблицы, ...)
| SELECT поле_таблицы, ... FROM имя_таблицы ...
```

Vērtības var ievietot, uzskaitot tās, izmantojot atslēgvārdu `VALUES`, norādot tās iekavās, atdalot tās ar komatiem, vai izmantojot `SELECT`.

Jauno ierakstu pievienošana iespējama 2 veidos:

- izmantojot sintaksi `INSERT INTO ... SELECT`

```sql
INSERT INTO Goods (good_id, good_name, type)
SELECT 20, 'Table', 2;
```

- izmantojot sintaksi `INSERT INTO ... VALUES (...)`

```sql
INSERT INTO Goods (good_id, good_name, type)
VALUES (20, 'Table', 2);
```

<mark style="background: #ADCCFFA6;">Viena komanda pievieno vienu ierakstu.</mark>

Ja vēlies ierakstīt vairākus ierakstus viena vaicājuma ietvaros, tad rīkojies šādi:

```sql
INSERT INTO Goods (good_id, good_name, type)
VALUES (20, 'Table', 2), (30, 'Chair'), (10, 'Lamp');
```

Vienkārši atdfali vienu ierakstu no cita caur `,` komatu.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[SQL īsa pamācība - tabulas izveide un dzēšana]]
Nākama lapa >>> [[SQL īsa pamācība - datu attēlošana SELECT]]

___