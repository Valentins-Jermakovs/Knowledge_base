___

**Datums:** 2025-08-04   
**Laiks:** 11:05 

❚ **Tagi:** #SQL 
⌬ **Priekšmets:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Datu izvade

Izmantojot operatoru `SELECT` var ne tikai nolasīt datus no tabulas, bet arī izvadīt tekstu.

```SQL
SELECT "Hello world"
```
#### Visu datu izvade no tabulas

Lai izvadīt datus no tabulas, izmanto šādu sintaksi:

```SQL
SELECT * FROM tabulas_nosaukums
```

Kur `*` saka parādīt visu informāciju.
##### Datu izvade no konkrētām kolonnām

Lai izvadīt tikai konkrētas kolonnas, raksti tās caur komatu, kā piemērā:

```SQL
SELECT member_id, member_name FROM FamilyMembers
```

Kur:

- `member_id, member_name` ir kolonnu nosaukumi
- `FamilyMembers` ir tabulas nosaukums
#### Pseidonīmi (aliases)

Lai <mark style="background: #ADCCFFA6;">izvadā</mark> mainīt kādas kolonnas nosaukumu, izmanto operatoru `AS`:

```SQL
SELECT member_id, member_name AS Name FROM FamilyMembers
```

Šajā piemērā, kolonna ar nosaukumu `member_name` tiks izvadīta/attēlota kā `Name`.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[SQL īsa pamācība - datu ierakstīšana tabulas laukos]]
Nākama lapa >>> [[SQL īsa pamācība - unikālo datu attēlošana DISTINCT]]

___