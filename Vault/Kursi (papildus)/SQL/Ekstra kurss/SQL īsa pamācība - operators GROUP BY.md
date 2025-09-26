___

**Datums:** 2025-08-04   
**Laiks:** 12:37 

❚ **Tagi:** #SQL 
⌬ **Priekšmets:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Grupēšana

Operators `GROUP BY` ļauj grupēt ierakstus pēc kategorijām, kolonnām. Grupēšana apvieno vairākus ierakstus, kas attiecināmi uz vienu kolonnu/kategoriju.

```SQL
SELECT [литералы, агрегатные_функции, поля_группировки]
FROM имя_таблицы
GROUP BY поля_группировки;
```

Konkrētāks piemērs, kas grupēs pēc laukiem `home_type`.

```SQL
SELECT home_type FROM Rooms
GROUP BY home_type
```

![[Pasted image 20250627191234.png]]

Grupēšana pēc `home-type`

![[groupping_by_1_field.webp]]

Grupēšana pēc `home_type` un `has_tv`

![[groupping_by_2_field.webp]]

```SQL
SELECT home_type, has_tv FROM Rooms
GROUP BY home_type, has_tv
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[SQL īsa pamācība - Agregātas funkcijas]]
Nākama lapa >>> [[Navigācija - SQL]]

___