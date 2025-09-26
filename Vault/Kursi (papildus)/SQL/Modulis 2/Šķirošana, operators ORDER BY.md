___
**Datums:** 2025-06-27   
**Laiks:** 18:46 
❚ **Tagi:** #SQL
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Operators ORDER BY
```SQL
SELECT поля_таблиц FROM наименование_таблицы
WHERE ...
ORDER BY столбец_1 [ASC | DESC][, столбец_n [ASC | DESC]]
```

Kur `ASC` un `DESC` - šķirošanas virzieni.
`ASC` - šķiro augošā secībā.
`DESC` - šķiro dilstošā.

Piemērs, izvadīt aviokompāniju nosaukumus alfabēta secībā:

```SQL
SELECT name FROM Company ORDER BY name;
```
#### Šķirošana dažādiem datu tipiem

| Datu tips       | ASC                           | DESC                          |
| --------------- | ----------------------------- | ----------------------------- |
| Teksta rinda    | `A-Z` un `a-z`                | `Z-A` un `z-a`                |
| Skaitļi         | No mazāka uz lielāko          | No lielāka uz mazāko          |
| Datums un laiks | No agrāka datuma līdz vecākam | No vecāka līdz sākuma datumam |
#### Šķirošana pēc vairākām kolonnām
```SQL
...ORDER BY столбец_1 [ASC | DESC], столбец_2 [ASC | DESC];
```

---
### ⇄ Saistības
Avots >>> [Сортировка, оператор ORDER BY — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/sorting)
Iepriekšēja lapa >>> [[Operators REGEXP]]
Nākama lapa >>> [[Grupēšana, GROUP BY]]
___