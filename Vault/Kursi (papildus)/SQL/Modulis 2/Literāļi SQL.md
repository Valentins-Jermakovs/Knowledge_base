___
**Datums:** 2025-06-27   
**Laiks:** 14:37 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Literāļi

> [!NOTE] Literālis
> Literālis ir skaidri norādīta fiksēta vērtība, piemēram, skaitlis 12 vai virkne "SQL".

Pamata literāļi:
- teksta rinda
- skaitļi
- loģiskais
- NULL
- datums un laiks
#### Teksta rindas literāļi
Teksta rinda ir viss, kas ietverts pēdiņās `"` vai `'` Šeit arī eksistē simboli, kas sākas ar `\`, piemēram `\n`, kas norāda uz jauno rindu:

```SQL
SELECT "Строка \n Другая строка" as String
```

#### Skaitļu literāļi

|                                                                                    | Piemērs                          |
| ---------------------------------------------------------------------------------- | -------------------------------- |
| Ietver sevī kā veselus, tā arī daļskaitļus. Daļskaitļiem tiek izmantots punkts `.` | `1`, `2.9`, `0.01`               |
| Var būt tikai vesels, daļskaitlis, vai viss uzreiz                                 | `.2`, `1.1`, `10`                |
| Var būt kā `pozitīvs`, tā arī `negatīvs`                                           | `+1`, `-10`, `-2.2`              |
| Var tikt attēlots eksponences veidā                                                | `1e3` (=1000)<br>`1e-3` (=0.001) |
#### Aritmētiskie operatori
Skaitļu literāļiem SQL valodā tiek izmantoti ierastie aritmētiskie operatori.

| Operators  | Apraksts                | Piemērs         |
| ---------- | ----------------------- | --------------- |
| `%`, `MOD` | Dalīšana uz nulli       | `11 % 5 = 1`    |
| `*`        | Reizināšana             | `10 * 16 = 160` |
| `+`        | Saskaitīšana            | `98 + 2 = 100`  |
| `-`        | Atņemšana               | `50 - 51 = -1`  |
| `/`        | Dalīšana                | `1 / 2 = 0.5`   |
| `DIV`      | Veselo skaitļu dalīšana | `10 DIV 4 = 2`  |
Izmantojot šos operatorus, var veikt dažādas aritmētiskas operācijas.

```SQL
SELECT (5 * 2 - 6) / 2 AS Result;
```

Izvads būs `2`.
#### Literāļi datumam un laikam
Datumu, laiku var attēlot kā teksta rindu vai skaitļus. Piemēram, `"1970-12-30"`, `"19701230"` un kā skaitlis `19701230`. Visos variantos tas tiks interpretēts kā 30. decembris, 1970. gads.

```SQL
SELECT * FROM FamilyMembers WHERE birthday > '1970-12-30'
```


|                 | Apraksts                                          | Formāts                                                                                           |
| --------------- | ------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| Datums          | Interpretējas kā datums ar laiku, kas vienāds `0` | `YYYY-MM-DD`, `YYYYMMDD`<br>Piemēram:<br>`'2020-01-01'` = 1 января 2020, 00:00:00                 |
| Laiks           | Satur tikai laiku, bez konkrēta datuma            | `hh:mm:ss`, `hh:mm`, `hh`, `ss`<br>Piemērs: `12:11` = 12:11:00                                    |
| Datums un laiks | Datums ar iespēju uzdot konkrētu laiku            | `YYYY-MM-DD hh:mm:ss`, `YYYYMMDDhhmmss`<br>Piemēram: `'20200101183030'` = 1 января 2020, 18:30:30 |
#### Loģiskie literāļi
Tas ir `TRUE` vai `FALSE`. `TRUE` = 1, bet `FALSE` = 0.
#### NULL
`NULL` nozīmē kā datu nav.

---
### ⇄ Saistības
Avots >>> [Литералы — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/literals)
Iepriekšēja lapa >>> [[SQL pamata sintakse]]
Nākama lapa >>> [[Funkciju izmantošana]]
___