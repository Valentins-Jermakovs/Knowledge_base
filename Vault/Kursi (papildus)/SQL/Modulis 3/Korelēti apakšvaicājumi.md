___
**Datums:** 2025-06-30   
**Laiks:** 14:15 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Korelēti apakšvaicājumi
Visi iepriekšējie apakšvaicājumi, kurus mēs apsvērām, bija nekorelēti (neatkarīgi). Tos varēja izpildīt neatkarīgi no galvenā vaicājuma, un mēs varējām redzēt, ko tie atgrieza, pirms to rezultāts tika izmantots galvenajā vaicājumā. Korelēti apakšvaicājumi attiecas uz vienu vai vairākām galvenā vaicājuma kolonnām.

Šeit sanāk vaicājums vaicājumā, kas tiek izpildīts katru reizi, kad izpildās galvenais vaicājums. Piemērā skatīties vaicājumu iekavās.

```sql
SELECT FamilyMembers.member_name, (
    SELECT SUM(Payments.unit_price * Payments.amount)
    FROM Payments
    WHERE Payments.family_member = FamilyMembers.member_id
) AS total_spent
FROM FamilyMembers;
```

Šeit tiek meklēta visdārgākā prece, ko bija pircis katrs ģimenes loceklis.

```sql
SELECT FamilyMembers.member_name, (SELECT MAX(Payments.unit_price) FROM Payments WHERE Payments.family_member = FamilyMembers.member_id) AS good_price FROM FamilyMembers
```

---
### ⇄ Saistības
Avots >>> [Коррелированные подзапросы — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/correlated-subqueries)
Iepriekšēja lapa >>> [[Vairāku kolonnu apakšvaicājumi]]
Nākama lapa >>> [[Kopīga tabulas izteiksme, WITH priekšraksts]]
___