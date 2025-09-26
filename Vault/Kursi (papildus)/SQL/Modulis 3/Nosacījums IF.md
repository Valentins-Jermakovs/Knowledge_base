___
**Datums:** 2025-06-30   
**Laiks:** 15:33 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Funkcija `IF`
```sql
IF(условное_выражение, значение_1, значение_2);
```

Ja nosacījuma izteiksme, kas `IF` funkcijai nodota kā pirmais arguments, ir patiesa, funkcija atgriež `vērtību_1`, pretējā gadījumā tā `vērtību_2`.

#### Piemēri
```sql
SELECT IF(10 > 20, "TRUE", "FALSE");
```

![[Pasted image 20250630154610.png]]

Funkcijas var arī likt vienu otrā, imitējot `CASE` darbību:
```sql
SELECT id, price,
    IF(price >= 200, "Бизнес-класс",
        IF(price >= 150,
            "Комфорт-класс", "Эконом-класс")) AS category
    FROM Rooms
```

#### Funkcijas `IFNULL` un `NULLIF`

#### `IFNULL` sintakse

```sql
IFNULL(значение, альтернативное_значение);
```

Funkcija `IFNULL` atgriež vērtību, kas nodota kā pirmais arguments, ja tā nav `NULL`, pretējā gadījumā tā atgriež `alternatīvo_vērtību`.

#### `NULLIF` sintakse

```sql
NULLIF(значение_1, значение_2);
```

Funkcija `NULLIF` atgriež `NULL`, ja `vērtība_1` ir vienāda ar `vērtību_2`, pretējā gadījumā tā atgriež `vērtību_1`.

```sql
SELECT NULLIF("SQL Academy", "SQL Academy") AS sql_trainer;
```

![[Pasted image 20250630155642.png]]

```sql
SELECT NULLIF("SQL Academy", "Альтернатива SQL Academy") AS sql_trainer;
```

![[Pasted image 20250630155705.png]]

#### Praktiskais piemērs

```sql
SELECT 
  Teacher.first_name, 
  Teacher.last_name, 
  IF(Teacher.middle_name IS NULL, 'Empty', Teacher.middle_name) AS middle_name
FROM Teacher;
```

`IF` funkcijai, ievadi nosacījumu un 2 argumentus.

---
### ⇄ Saistības
Avots >>> [Условная функция IF — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/if-function)
Iepriekšēja lapa >>> [[Loģika, CASE operators]]
Nākama lapa >>> [[Navigācija - SQL]]
___