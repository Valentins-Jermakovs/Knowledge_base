___
**Datums:** 2025-06-27   
**Laiks:** 19:24 
❚ **Tagi:** #SQL
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Agregātas funkcijas

> [!NOTE] Agregāta funkcija
> Tā ir funkcija, kas veic aprēķinu vērtību kopai un atgriež vienu vērtību.
#### Kopēja vaicājuma struktūra
```SQL
SELECT [литералы, агрегатные_функции, поля_группировки]
FROM имя_таблицы
GROUP BY поля_группировки;
```

Piemēram, funkcijas `AVG` izmantošana:

```SQL
SELECT home_type, AVG(price) as avg_price FROM Rooms
GROUP BY home_type
```
#### Funkciju apraksts

| Funkcija              | Apraksts                  |
| --------------------- | ------------------------- |
| `SUM(поле_таблицы)`   | Atgriež summu             |
| `AVG(поле_таблицы)`   | Atgriež vidējo vērtību    |
| `COUNT(поле_таблицы)` | Atgriež ierakstu daudzumu |
| `MIN(поле_таблицы)`   | Atgriež minimālo vērtību  |
| `MAX(поле_таблицы)`   | Atgriež maksimālo vērtību |
>Agregātas funkcijas tiek izmantotas vērtībām, kas nav vienādas ar `NULL`. Izņēmumā gadījums ir funkcija `COUNT(*)`.

---
### ⇄ Saistības
Avots >>> [Агрегатные функции — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/aggregate-functions)
Iepriekšēja lapa >>> [[Grupēšana, GROUP BY]]
Nākama lapa >>> [[Operators HAVING]]
___