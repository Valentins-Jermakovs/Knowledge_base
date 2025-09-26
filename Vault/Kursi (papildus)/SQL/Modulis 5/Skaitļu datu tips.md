___
**Datums:** 2025-07-01   
**Laiks:** 14:45 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Skaitļu datu tips

Standarta aritmētiskas operācijas:
- `+`
- `-`
- `*`
- `/`

```sql
SELECT 2 * ((22 - 16) / (2 + 1)) AS calc_example;
```

#### Matemātiskas funkcijas

| Funkcija          | Apraksts                               |
| ----------------- | -------------------------------------- |
| `POW(num, power)` | Ceļ norādītajā pakāpē                  |
| `SQRT(num)`       | Aprēķina kvadrātsakni                  |
| `LOG(base, num)`  | Aprēķina logaritmu pēc norādītas bāzes |
| `EXP(num)`        | Aprēķina enum                          |
| `SIN(num)`        | Aprēķina sīnusu                        |
| `COS(num)`        | Aprēķina kosīnusu                      |
| `TAN(num)`        | Aprēķina tangensu                      |
#### Skaitļu noapaļošana

Funkcijas noapaļošanai
- `CEIL` - noapaļo uz lielāko veselu skaitli
- `FLOOR` - noapaļo uz mazāko veselo skaitli
- `ROUND` - ja `>= 5`, noapaļo uz augšu, ja nē, tad uz leju
- `TRUNCATE` - dara to pašu

Funkcija `SIGN` atgriež `-1`, ja skaitlis negatīvs, `0`, ja nulle un `1`, ja pozitīvs.

Funkcija `ABS` atgriež absolūto vērtību.

![[Pasted image 20250701145621.png]]

---
### ⇄ Saistības
Avots >>> [Числовой тип данных — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/work-with-number-data-type)
Iepriekšēja lapa >>> [[Navigācija - SQL]]
Nākama lapa >>> [[Datums un laiks]]
___