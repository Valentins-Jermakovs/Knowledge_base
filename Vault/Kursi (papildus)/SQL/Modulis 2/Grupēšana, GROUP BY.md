___
**Datums:** 2025-06-27   
**Laiks:** 19:09 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Grupēšana
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
Avots >>> [Группировка, оператор GROUP BY — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/groupping)
Iepriekšēja lapa >>> [[Šķirošana, operators ORDER BY]]
Nākama lapa >>> [[Agregātas funkcijas]]
___