___
**Datums:** 2025-07-01   
**Laiks:** 15:24 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Datu konvertācija

Lai konvertēt datus no viena tipa uz otru, tiek izmantoti operatori `CAST`, `CONVERT`.

```sql
CAST(значение AS тип_для_конвертации);
CONVERT(значение, тип_для_конвертации);
```

Praktisks piemērs
```sql
SELECT CAST(12005.6 AS DECIMAL), CONVERT(12005.4, DECIMAL);
```

| Tips               | Apraksts                                                                                                    |
| ------------------ | ----------------------------------------------------------------------------------------------------------- |
| `DATE`             | Konvertē uz `YYYY-MM-DD`                                                                                    |
| `DATETIME`         | Konvertē uz `YYYY-MM-DD hh"mm:ss`                                                                           |
| `TIME`             | Konvertē uz `hh:mm:ss`                                                                                      |
| `DECIMAL[(M[,D])]` | Konvertē uz `DECIMAL`. Ir 2 neobligāti argumenti, kas nosaka maksimālu simbolu daudzumu līdz un pēc komata. |
| `CHAR[(N)]`        | Konvertē uz `CHAR`. Neobligātais arguments `N` nosaka teksta rindas maksimālo garumu.                       |
| `SIGNED`           | Konvertē uz `BIGINT`                                                                                        |
| `UNSIGNED`         | Konvertē uz bezzīmi `BIGINT`                                                                                |
| `BINARY`           | Konvertē uz `BINARY`                                                                                        |
| `YEAR`             | Konvertē uz gadu                                                                                            |


---
### ⇄ Saistības
Avots >>> [Функции преобразования типов, CAST — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/type-conversion-functions)
Iepriekšēja lapa >>> [[Datums un laiks]]
Nākama lapa >>> [[Loga funkcijas]]
___