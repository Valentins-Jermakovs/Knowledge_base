___
**Datums:** 2025-06-30   
**Laiks:** 15:18 
❚ **Tagi:** #SQL
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Operators `CASE`
Pēc principa līdzīgs `switch-case` blokiem programmēšanā.

```sql
CASE
    WHEN условие_1 THEN возвращаемое_значение_1
    WHEN условие_2 THEN возвращаемое_значение_2
    WHEN условие_n THEN возвращаемое_значение_n
    [ELSE возвращаемое_значение_по_умолчанию]
END
```

```sql
SELECT first_name, last_name,
CASE
  WHEN TIMESTAMPDIFF(YEAR, birthday, NOW()) >= 18 THEN "Совершеннолетний"
  ELSE "Несовершеннолетний"
END AS status
FROM Student
```

Praktiskais piemērs, izvadīt teksta paziņojumu atkarībā no reitinga:
```sql
SELECT Reviews.id,
CASE
    WHEN Reviews.rating BETWEEN 4 AND 5 THEN "positive"
    WHEN Reviews.rating = 3 THEN "neutral"
    WHEN Reviews.rating BETWEEN 1 AND 2 THEN "negative"
END AS rating
FROM Reviews
```

---
### ⇄ Saistības
Avots >>> [Условная логика, оператор CASE — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/case-expression)
Iepriekšēja lapa >>> [[Vaicājumu apvienošana]]
Nākama lapa >>> [[Nosacījums IF]]
___