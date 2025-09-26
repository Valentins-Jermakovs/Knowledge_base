___

**Datums:** 2025-08-04   
**Laiks:** 11:21 

❚ **Tagi:** #SQL 
⌬ **Priekšmets:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Operators ORDER BY

```SQL
SELECT поля_таблиц FROM наименование_таблицы
WHERE ...
ORDER BY столбец_1 [ASC | DESC][, столбец_n [ASC | DESC]]
```

Kur `ASC` un `DESC` - šķirošanas virzieni:

- `ASC` - šķiro augošā secībā;
- `DESC` - šķiro dilstošā.

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

Iepriekšēja lapa >>> [[SQL īsa pamācība - datu izvades ierobežošana LIMIT]]
Nākama lapa >>> [[SQL īsa pamācība - jaunās kolonnas pievienošana esošai tabulai ALTER TABLE]]

___