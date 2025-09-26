___
**Datums:** 2025-06-27   
**Laiks:** 16:26 
❚ **Tagi:** #SQL
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### IS NULL
Operators `IS NULL` ļauj uzzināt, vai pārbaudāma vērtība ir `NULL`

```SQL
SELECT * FROM Teacher
WHERE middle_name IS NULL;
```

Taču ja mēs gribam atrast, kur lauki <mark style="background: #ADCCFFA6;">nav vienādi</mark> ar `NULL`:

```SQL
SELECT * FROM Teacher
WHERE middle_name IS NOT NULL;
```
#### BETWEEN
Operators `BETWEEN min AND max` ļauj uzzināt, vai vērtība atrodas diapazonā starp `min` un `max`.

Pēc būtības tas esot identisks šādam vaicājumam:

```SQL
... WHERE field >= min AND field <= max
```

Operatora izmantošanas piemērs:
```SQL
SELECT * FROM Payments
WHERE unit_price BETWEEN 100 AND 500;
```
#### IN
Operators `IN` ļauj uzzināt, vai meklējama vērtība atrodas sarakstā.

```SQL
SELECT * FROM FamilyMembers
WHERE status IN ('father', 'mother');
```

---
### ⇄ Saistības
Avots >>> [Операторы IS NULL, BETWEEN, IN — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/is-null-between-in-operators)
Iepriekšēja lapa >>> [[Operators WHERE]]
Nākama lapa >>> [[Operators LIKE]]
___