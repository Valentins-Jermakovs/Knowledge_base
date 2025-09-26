___
**Datums:** 2025-07-02   
**Laiks:** 14:07 
❚ **Tagi:** #SQL
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Bloķēšana

**1. Tabulas bloķēšana (Table Lock):**  
Lietotāji nevar vienlaicīgi mainīt datus vienā tabulā. Vienkārši īstenojama, bet var radīt gaidīšanas laiku pie daudziem lietotājiem.

**2. Lapas bloķēšana (Page Lock):**  
Bloķē konkrētu atmiņas segmentu (2–16 KB) tabulā. Efektīvāka nekā visa tabulas bloķēšana, bet sarežģītāka.

**3. Rindas bloķēšana (Row Lock):**  
Bloķē tikai konkrēto rindu tabulā. Ļauj daudziem lietotājiem vienlaikus strādāt ar dažādām rindām. Lēnāka, bet visprecīzākā un elastīgākā.

---
### ⇄ Saistības
Avots >>> [Блокировки в СУБД — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/locking)
Iepriekšēja lapa >>> [[Navigācija - SQL]]

___