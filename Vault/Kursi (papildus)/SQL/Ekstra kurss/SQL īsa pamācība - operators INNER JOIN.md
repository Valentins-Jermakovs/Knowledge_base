___

**Datums:** 2025-08-04   
**Laiks:** 12:22 

❚ **Tagi:** #SQL 
⌬ **Priekšmets:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Iekšējs savienojums

Struktūras piemērs:

```sql
SELECT поля_таблиц FROM таблица_1
[INNER] JOIN таблица_2
    ON условие_соединения
[INNER] JOIN таблица_n
    ON условие_соединения
```

> [!NOTE] Iekšējs savienojums
> Iekšējais savienojums ir savienojums, kas atrod ierakstu pārus no divām tabulām, kas atbilst savienojuma nosacījumam, tādējādi izveidojot jaunu tabulu, kas satur laukus no pirmās un otrās avota tabulas.

![[inner-join-example.webp]]
#### WHERE izmantošana tabulu apvienošanai

Apvienot tabulas var arī ar `WHERE` operatoru:

```sql
SELECT family_member, member_name FROM Payments, FamilyMembers
    WHERE Payments.family_member = FamilyMembers.member_id
```
#### Praktiskais piemērs

```sql
SELECT G.good_name FROM Payments AS P
INNER JOIN FamilyMembers AS F
    ON P.family_member = F.member_id
INNER JOIN Goods AS G
    ON P.good = G.good_id
WHERE F.status = 'son'
```

Šis SQL vaicājums **apvieno trīs tabulas** – `Payments`, `FamilyMembers` un `Goods` , lai atrastu to preču nosaukumus (`G.good_name`), kuras ir iegādājies ģimenes loceklis ar statusu **"son"**.

 **Savienojumu secība un jēga:**
 
1. **`Payments AS P`** – pamattabula, kur glabājas informācija par pirkumiem: kurš (family_member) un ko (good) ir iegādājies;
2. **`INNER JOIN FamilyMembers AS F ON P.family_member = F.member_id`** – pievieno informāciju par to, kurš veica pirkumu (piemēram, dēls, māte u.c.);
3. **`INNER JOIN Goods AS G ON P.good = G.good_id`** – pievieno informāciju par to, kāda prece tika iegādāta;
4. **`WHERE F.status = 'son'`** – filtrē tikai tos gadījumus, kad pirkumu veicis dēls.

<mark style="background: #FF5582A6;">Sākumā definē tabulas, pēc tam izmanto.</mark>

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[SQL īsa pamācība - operators JOIN]]
Nākama lapa >>> [[SQL īsa pamācība - operators OUTER JOIN]]

___