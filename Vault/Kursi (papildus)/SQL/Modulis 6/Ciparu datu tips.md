___
**Datums:** 2025-07-02   
**Laiks:** 12:46 
❚ **Tagi:** #SQL
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Ciparu datu tipi

| **Tips**                                | **Atmiņas apjoms** | **Vērtību diapazons**                                                           | **Apraksts**                             |
| --------------------------------------- | ------------------ | ------------------------------------------------------------------------------- | ---------------------------------------- |
| **Precīzi veselie skaitļi**             |                    |                                                                                 |                                          |
| `TINYINT`                               | 1 baits            | Parakstīts: -128 līdz 127 Bez zīmes: 0 līdz 255                                 | Mazākie veselie skaitļi                  |
| `SMALLINT`                              | 2 baiti            | Parakstīts: -32 768 līdz 32 767 Bez zīmes: 0 līdz 65 535                        | Nelieli veselie skaitļi                  |
| `MEDIUMINT`                             | 3 baiti            | Parakstīts: -8 388 608 līdz 8 388 607 Bez zīmes: 0 līdz 16 777 215              | Vidēji lieli veselie                     |
| `INT` / `INTEGER`                       | 4 baiti            | Parakstīts: -2³¹ līdz 2³¹-1 Bez zīmes: 0 līdz 4 294 967 295                     | Biežāk izmantotais tips                  |
| `BIGINT`                                | 8 baiti            | Parakstīts: -2⁶³ līdz 2⁶³-1 Bez zīmes: 0 līdz 2⁶⁴-1                             | Ļoti lieli veselie                       |
| **Precīzi decimālskaitļi**              |                    |                                                                                 |                                          |
| `DEC(M,D)`,`DECIMAL(M,D)`               | Atkarīgs no M un D | Atkarībā no norādītajiem parametriem (piem. DECIMAL(5,2) → -999.99 līdz 999.99) | Lieto finanšu datiem, augsta precizitāte |
| **Bitu dati**                           |                    |                                                                                 |                                          |
| `BIT(M)`                                | M biti (1–64)      | Binārā virkne, piem.: `BIT(6)` var glabāt vērtību `b'000101'`                   | Fiksēts bitu skaits                      |
| `BOOL`, `BOOLEAN`                       | 1 bits             | 0 vai 1                                                                         | Loģiska vērtība                          |
| **Aptuvenie skaitļi (plūstošā punkta)** |                    |                                                                                 |                                          |
| `FLOAT(M,D)`                            | 4 baiti            | ±1.17·10⁻³⁹ līdz ±3.4·10³⁸                                                      | Mazāka precizitāte                       |
| `REAL(M,D)`,`DOUBLE(M,D)`               | 8 baiti            | ±2.22·10⁻³⁰⁸ līdz ±1.79·10³⁰⁸                                                   | Augsta precizitāte                       |

- **UNSIGNED** atribūts liedz negatīvu vērtību glabāšanu un palielina pozitīvo intervālu (veselajiem).
- `DECIMAL` saglabā ciparus kā 2 veselus skaitļus: pirms un pēc komata.
- `FLOAT` un `DOUBLE` atbalsta `UNSIGNED`, bet tas nemaina maksimālo diapazonu – tikai neļauj negatīvas vērtības.

---
### ⇄ Saistības
Avots >>> [Числовой тип данных — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/number-data-type)
Iepriekšēja lapa >>> [[Teksta rindas datu tips]]
Nākama lapa >>> [[Datuma un laika tipi]]
___