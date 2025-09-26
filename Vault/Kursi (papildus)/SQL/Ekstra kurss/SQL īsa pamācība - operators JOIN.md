___

**Datums:** 2025-08-04   
**Laiks:** 12:19 

❚ **Tagi:** #SQL 
⌬ **Priekšmets:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Tabulu apvienošana

Operators `JOIN` tiek izmantots, lai vienā pieprasījumā apvienot\izmantot vairākas tabulas kopā.

Kopēja pieprasījuma struktūra/sintakse:

```SQL
SELECT поля_таблиц
FROM таблица_1
[INNER] | [[LEFT | RIGHT | FULL][OUTER]] JOIN таблица_2
    ON условие_соединения
[[INNER] | [[LEFT | RIGHT | FULL][OUTER]] JOIN таблица_n
    ON условие_соединения]
```

`INERR` - iekšējs savienojums

`OUTER` - ārējs savienojums. 
Ārējs savienojums dalās uz kreiso `LEFT` un labo `RIGHT`, kā arī pilno `FULL`.

Šeit piemērs ar iekšējo savienojumu:

```SQL
SELECT family_member, member_name, amount * unit_price AS price FROM Payments
INNER JOIN FamilyMembers
    ON Payments.family_member = FamilyMembers.member_id
```

Šis pieprasījums apvieno tabulas `Payments` un `FamilyMembers`. Pēc nosacījuma sanāk ka kolonna `family_member` no `Payments` ir vienāda ar kolonnu `member_id` no tabulas `FamilyMembers`. Tādējādi tiek parādīts, kas veica pirkumu, atbilstoši indeksam.

| JOIN tipi    | Skaidrojums                                                                                                         |
| ------------ | ------------------------------------------------------------------------------------------------------------------- |
| `INNER JOIN` | Ja 2 tabulu ieraksti sakrīt, tad tie tik atrādīti abi. Ja kāds no vienas tabulas ierakstiem ir tukšs, izvada nebūs. |
| `LEFT JOIN`  | Atgriež visu no kreisās tabulas, ja labai ieraksts nesakrīt, tad labajā izvadīs `NULL`                              |
| `RIGHT JOIN` | Analoģisks `LEFT JOIN`, bet primāra ir labā tabula                                                                  |
| `FULL JOIN`  | Atgriež abas tabulas. bet ja sakritību vienā no tabulām nav, tad atgriež `NULL`                                     |

```SQL
SELECT p.id, p.name FROM Passenger AS p
INNER JOIN Pass_in_trip AS pit
    ON pit.passenger = p.id;
```

Šajā piemērā tiek izmantoti `aliasi`, lai būtu vienkāršāk saprast.
#### Visu ierakstu izvade no vairākām tabulām

Agrāk, lai izvadīt visas tabulas kolonnas, tika izmantots simbols `*`. Tagad, kad tabulu ir vairāk, vienkārši norādi tabulas nosaukumu un caur punktu pievieno `*`.

```SQL
SELECT FamilyMembers.* FROM Payments
INNER JOIN FamilyMembers
    ON Payments.family_member = FamilyMembers.member_id
```

```sql
SELECT Payments.*, FamilyMembers.* FROM Payments
INNER JOIN FamilyMembers
    ON Payments.family_member = FamilyMembers.member_id
```

Piemērs, kad vajag izvadīt 2 kolonnas no vienas tabulas un visu otro tabulu:

```sql
SELECT payment_id, family_member, FamilyMembers.* FROM Payments
INNER JOIN FamilyMembers
    ON Payments.family_member = FamilyMembers.member_id
```

Vienkārši norādi vajadzīgas kolonnas izvadam manuāli.
#### Pseidonīmi tabulām - aliasi

Tas pats operators `AS`, bet tagad tas tiek izmantots pret tabulām

```sql
SELECT id, name
FROM Passenger AS pass
```

```sql
SELECT
    pass.id,
    pass.name
FROM Passenger AS pass
INNER JOIN Pass_in_trip AS pit
    ON pit.passenger = pass.id
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[SQL īsa pamācība - operators DELETE]]
Nākama lapa >>> [[SQL īsa pamācība - operators INNER JOIN]]

___