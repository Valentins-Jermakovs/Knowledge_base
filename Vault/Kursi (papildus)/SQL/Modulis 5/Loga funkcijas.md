___
**Datums:** 2025-07-01   
**Laiks:** 16:49 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Loga funkcijas
Logu funkcijas ir spēcīgs SQL valodas rīks, kas ļauj veikt sarežģītus aprēķinus rindu grupām, kas ir saistītas ar pašreizējo rindu.

![[schema_table.webp]]

![[2.webp]]

![[3.webp]]

![[4.webp]]

```sql
SELECT <оконная_функция>(<поле_таблицы>)
OVER (
      [PARTITION BY <столбцы_для_разделения>]
      [ORDER BY <столбцы_для_сортировки>]
      [ROWS|RANGE <определение_диапазона_строк>]
)
```

- `PARTITION BY` – sadala rindas grupās.
- `ORDER BY` – nosaka secību katrā logā.
- `ROWS` vai `RANGE` – nosaka, kuras rindas ietilpst logā.

![[query-order.webp]]

#### Praktiskais piemērs
Uzdevums: saskaitīt, cik skolēnu ir katrā klasē.
```sql
SELECT
  Student.first_name,
  Student.last_name,
  Student_in_class.class,
  COUNT(*) OVER (PARTITION BY Student_in_class.class) AS student_count_in_class
FROM
  Student_in_class
JOIN Student ON Student_in_class.student = Student.id;
```

Šeit:
- `PARTITION BY class` sadala rindas pēc klases.
- `COUNT(*)` saskaita skolēnus katrā klasē, atstājot katru skolēnu kā atsevišķu rindu.

#### Atšķirība no grupēšanas funkcijām
**Grupēšanas funkcijas** (piem., `GROUP BY`) atgriež vienu rindu uz grupu.
**Logfunkcijas** atgriež vienu rindu uz katru ierakstu, ar papildu informāciju kolonnā.

---
### ⇄ Saistības
Avots >>> [Оконные функции — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/windows-functions)
Iepriekšēja lapa >>> [[Funkcija CAST]]
Nākama lapa >>> [[Pārtīcijas logu funkcijās]]
___