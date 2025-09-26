___
**Datums:** 2025-06-30   
**Laiks:** 11:16 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Vienas rindas vienas kolonnas apakšvaicājums
Šāda veida apakšvaicājums ir pazīstams arī kā skalārs apakšvaicājums.
To var izmantot dažādās galvenā SQL vaicājuma daļās, bet visbiežāk to izmanto vaicājumu ierobežojumos, izmantojot salīdzināšanas operatorus (`=`, `<>`, `>`, `<`).
#### Piemēri

Šis piemērs demonstrē vienas rindas izvadu.

```sql
SELECT (SELECT name FROM company LIMIT 1) AS company_name;
```

Tāpat šādus vaicājumus var izmantot filtrācijai, ar operatoru `WHERE`

```sql
SELECT * FROM FamilyMembers
    WHERE birthday = (SELECT MAX(birthday) FROM FamilyMembers);
```

---
### ⇄ Saistības
Avots >>> [Подзапросы с одной строкой с одним столбцом — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/subquery-with-one-column-one-row)
Iepriekšēja lapa >>> [[Apakšvaicājums]]
Nākama lapa >>> [[Apakšvaicājumi ar vairākām rindām un vienu kolonnu]]
___