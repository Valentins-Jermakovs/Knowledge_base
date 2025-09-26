___

**Datums:** 2025-08-04   
**Laiks:** 12:33 

❚ **Tagi:** #SQL 
⌬ **Priekšmets:**  `SQL`

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

Iepriekšēja lapa >>> [[SQL īsa pamācība - operators OUTER JOIN]]
Nākama lapa >>> [[SQL īsa pamācība - operators GROUP BY]]

___