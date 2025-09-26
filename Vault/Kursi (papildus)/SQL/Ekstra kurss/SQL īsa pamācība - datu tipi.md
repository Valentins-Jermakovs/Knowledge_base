___

**Datums:** 2025-08-04   
**Laiks:** 10:29 

❚ **Tagi:** #SQL 
⌬ **Priekšmets:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Datu tipi

`SQL` pastāv vairāki datu tipi, kas tiek izmantoti tabulas izveides laikā. Katrai DB vadības programmai ir savs unikāls dialekts, un datu tipi, to formas var atšķirties, bet kopumā pastāv šāds vispārīgs standarts.

##### SQL datu tipi - tekstveide

|Datu tips|Apraksts|
|---|---|
|`CHAR(size)`|Fiksēta garuma teksts (līdz 255 rakstzīmēm).|
|`VARCHAR(size)`|Mainīga garuma teksts (līdz 255 rakstzīmēm).|
|`TINYTEXT`|Teksts līdz 255 rakstzīmēm.|
|`TEXT`|Teksts līdz 65 535 rakstzīmēm.|
|`BLOB`|Bināri dati līdz 65 535 baitiem.|
|`MEDIUMTEXT`|Teksts līdz 16 777 215 rakstzīmēm.|
|`MEDIUMBLOB`|Bināri dati līdz 16 777 215 baitiem.|
|`LONGTEXT`|Teksts līdz 4 294 967 295 rakstzīmēm.|
|`LONGBLOB`|Bināri dati līdz 4 294 967 295 baitiem.|
|`ENUM(x, y, ...)`|Saraksts ar iespējām (līdz 65 535 vērtībām). Ja ievadītā vērtība nav sarakstā — tiek saglabāta `NULL`.|
|`SET`|Saraksts līdz 64 vērtībām; var izvēlēties vairākas vienlaicīgi.|

##### SQL datu tipi - skaitļi

|Datu tips|Vērtību diapazons / apraksts|
|---|---|
|`TINYINT`|-128 līdz 127|
|`SMALLINT`|-32 768 līdz 32 767|
|`MEDIUMINT`|-8 388 608 līdz 8 388 607|
|`INT`|-2 147 483 648 līdz 2 147 483 647|
|`BIGINT`|-9 223 372 036 854 775 808 līdz 9 223 372 036 854 775 807|
|`FLOAT(size,d)`|Reāls skaitlis ar mazu precizitāti.|
|`DOUBLE(size,d)`|Reāls skaitlis ar dubultu precizitāti.|
|`DECIMAL(size,d)`|Precīzs decimālskaitlis, glabājas kā teksts.|

##### SQL datu tipi - datums un laiks

|Datu tips|Formāts|
|---|---|
|`DATE`|`GGGG-MM-DD`|
|`DATETIME`|`GGGG-MM-DD HH:MM:SS`|
|`TIMESTAMP`|Unix laika zīmogs, bet attēlojas kā `GGGG-MM-DD HH:MM:SS`|
|`TIME`|`HH:MM:SS`|
|`YEAR`|Gads (`GG` vai `GGGG`)|

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[SQL īsa pamācība - savienojumu veidi]]
Nākama lapa >>> [[SQL īsa pamācība - datu bāzes izveide un dzēšana]]

___