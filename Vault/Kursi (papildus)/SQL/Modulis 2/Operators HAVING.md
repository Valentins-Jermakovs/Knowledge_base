___
**Datums:** 2025-06-27   
**Laiks:** 19:42 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Grupu filtrācija
Lai filtrēt grupas, izmanto operatoru `HAVING`.

```SQL
SELECT home_type, AVG(price) as avg_price FROM Rooms
GROUP BY home_type
HAVING avg_price > 50
```

![[Pasted image 20250627194521.png]]

![[sql_query_order_ru.webp]]
#### Kopēja vaicājuma struktūra ar operatoru HAVING
```SQL
SELECT [константы, агрегатные_функции, поля_группировки]
FROM имя_таблицы
WHERE условия_на_ограничения_строк
GROUP BY поля_группировки
HAVING условие_на_ограничение_строк_после_группировки
ORDER BY условие_сортировки
```
#### Piemērs HAVING izmantošanai
```SQL
SELECT home_type, MIN(price) as min_price FROM Rooms
WHERE has_tv = True
GROUP BY home_type
HAVING COUNT(*) >= 5;
```


---
### ⇄ Saistības
Avots >>> [Оператор HAVING — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/operator-having)
Iepriekšēja lapa >>> [[Agregātas funkcijas]]
Atpakaļ uz saturu >>> [[Navigācija - SQL]]
___