___

**Datums:** 2025-08-04   
**Laiks:** 11:48 

❚ **Tagi:** #SQL 
⌬ **Priekšmets:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Operators LIKE

Šis operators tiek izmantots, lai atrast ierakstus, kas atbilst konkrētam šablonam.

Sintakses piemērs:

```SQL
... WHERE поле_таблицы [NOT] LIKE шаблон_строки
```

| Simbols | Apraksts                                           |
| ------- | -------------------------------------------------- |
| `%`     | Simbolu virkne, nenoteiks jebkuru simbolu daudzums |
| `_`     | Jebkurš viens simbols                              |

**Piemēri**

```SQL
... WHERE поле_таблицы LIKE 'text%'
```

Meklēs visas teksta rindas, kas <mark style="background: #ADCCFFA6;">sākas</mark> ar `text`.

```SQL
... WHERE поле_таблицы LIKE '%text'
```

Meklēs visas teksta rindas, kas <mark style="background: #ADCCFFA6;">beidzās</mark> ar `text`.

```SQL
... WHERE поле_таблицы LIKE '_ext'
```

Meklē teksta rindas, kas ir `4` simbolus garas un beidzās ar `ext`.

```SQL
... WHERE поле_таблицы LIKE 'begin%end'
```

Meklē teksta rindas, kas <mark style="background: #ADCCFFA6;">sākas</mark> ar `begin` un <mark style="background: #ADCCFFA6;">beidzās</mark> ar `end`.

Tas tiek izmantots, kad mēs gribam uzzināt, vai meklējama teksta rinda pieder konkrētam šablonam. Piemēram ir `email`, un mums jāatrod e-pastus ar domēnu `@hotmail.`

```SQL
SELECT name, email FROM Users
WHERE email LIKE '%@hotmail.%'
```
#### ESCAPE-simbols

`ESCAPE-simbols` tiek izmantots, lai ekranēt speciālus simbolus (`%` un `\`).

```SQL
SELECT job_id FROM Jobs
WHERE progress LIKE '3!%' ESCAPE '!';
```

Šeit tiek meklēti ieraksti, kam `progress` ir `3%`.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[SQL īsa pamācība - datu atjaunošana, ierakstīšana UPDATE]]
Nākama lapa >>> [[SQL īsa pamācība - operators BETWEEN]]

___