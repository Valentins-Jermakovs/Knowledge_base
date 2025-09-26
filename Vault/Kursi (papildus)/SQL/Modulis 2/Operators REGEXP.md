___
**Datums:** 2025-06-27   
**Laiks:** 16:55 
❚ **Tagi:** #SQL
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Operators REGEXP
Salīdzinājumā ar `LIKE`, tas ļauj veidot sarežģītākus šablonus un izmantot speciālus simbolus.

Sintakse:

```SQL
... WHERE table_field REGEXP 'pattern';
```

Speciālie simboli:
- šādi simboli pieprasa ekranēšanu: `.`, `*`, `+`, `?`, `[`, `]`, `(`, `)`, `{`, `}`, `|`, `\`
- Ekranēšanai izmanto `\\`
#### Speciālie simboli un struktūras

| Simboli un struktūras | Kam ekvivalents                                                                                       |
| --------------------- | ----------------------------------------------------------------------------------------------------- |
| `*`                   | Atkārto iepriekšējo rakstu **0 vai vairāk reizes** (tas var nebūt vispār vai atkārtoties daudz reižu) |
| `+`                   | Atkārto iepriekšējo rakstu **vismaz 1 reizi**                                                         |
| `.`                   | Jebkurš **viens** simbols (burts, cipars, jebkas)                                                     |
| `?`                   | Iepriekšējais raksts var būt **vai nu 1 reizi, vai vispār nebūt**                                     |
| `^`                   | Atbilst **rindas sākumam**                                                                            |
| `$`                   | Atbilst **rindas beigām**                                                                             |
| `[abc]`               | Jebkurš **viens simbols no iekavās norādītajiem** (piemēram, `a`, `b` vai `c`)                        |
| `[^abc]`              | Jebkurš simbols, **izņemot tos, kas ir iekavās**                                                      |
| `[A-Z]`               | **Lielie burti** latīņu alfabētā                                                                      |
| `[a-z]`               | **Mazie burti** latīņu alfabētā                                                                       |
| `[0-9]`               | Jebkurš **viens cipars** no 0 līdz 9                                                                  |
| p1\|p2\|p3            | Atbilst jebkuram patternam, `p1`, `p2` vai `p3`                                                       |
| `{n}`                 | Tieši **n reižu** jāatkārto iepriekšējais raksts                                                      |
| `{m,n}`               | Jāatkārto iepriekšējais raksts vismaz **m reizes un ne vairāk kā n reizes**                           |

#### Piemēri
**Visi vārdi, kas sākas ar `John`.** Simbols `^` norāda uz teksta rindas sākumu.

```SQL
SELECT * FROM Users WHERE name REGEXP '^John'
```

**Visi priekšmeti, kas beidzās ar `e` vai `y`.** Šeit `[ey]` nosaka vērtību sarakstu, `$` norāda uz to, kā ar tiem simboliem teksta rindai jābeidzas (norāda beigas).

```SQL
SELECT * FROM  Subject WHERE name REGEXP '[ey]$'
```

**Visi e-pasti, kas beidzās ar `@outlook.com` vai `@icloud.com`.** `$` norāda rindas beigas, `|` ļauj norādīt vairākus patternu variantus.

```SQL
SELECT * FROM Users WHERE email REGEXP '@(outlook.com|icloud.com)$'
```

**Atrast visus lietotājus, kuru numurs nesatur `2` un `8`.** Šajā piemērā `[^28]` norāda visus simbolus, izņemot `2` un `8`, bet `*` norāda jebkuru daudzumu tādu simbolu. `^` un `$` norāda uz sākumu un beigām.

```SQL
SELECT * FROM Users WHERE phone_number REGEXP '^[^28]*$'
```

**Atrast visus lietotājus, kuru numurs sākas ar `+7`.** Šeit `^` norāda uz sākumu, tā kā `+` ir speciāla zīme, tā tiek ekranēta `\\+`.

```SQL
SELECT name, phone_number FROM Users WHERE phone_number REGEXP '^\\+7'
```

---
### ⇄ Saistības
Avots >>> [Оператор REGEXP — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/operator-regexp)
Iepriekšēja lapa >>> [[Operators LIKE]]
Nākama lapa >>> [[Šķirošana, operators ORDER BY]]
___