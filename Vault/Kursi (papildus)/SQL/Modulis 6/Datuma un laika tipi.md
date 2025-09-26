___
**Datums:** 2025-07-02   
**Laiks:** 12:51 
❚ **Tagi:** #SQL
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Datuma un laika tipi
|**Tips**|**Apraksts**|**Vērtību diapazons**|**Izmērs**|
|---|---|---|---|
|`DATE`|Glabā datumu `GGGG-MM-DD` formātā. Piemērs: `2022-12-05`|no `1000-01-01` līdz `9999-12-31`|3 baiti|
|`TIME`|Glabā laiku `HH:MM:SS` vai `HHH:MM:SS` formātā.Piemērs: `800:50:50`|no `-838:59:59` līdz `838:59:59`|3 baiti|
|`DATETIME`|Glabā datumu un laiku `GGGG-MM-DD HH:MM:SS` formātā.Piemērs: `2022-12-05 10:37:22`|no `1000-01-01 00:00:00` līdz `9999-12-31 23:59:59`|8 baiti|
|`TIMESTAMP`|Glabā datumu un laiku kā sekundes no `1970-01-01 00:00:01 UTC`.Piemērs: `2022-12-05 10:37:22`|no `1970-01-01 00:00:01` līdz `2038-01-19 03:14:07`|4 baiti|

#### Atšķirības starp `DATETIME` un `TIMESTAMP`

|**Parametrs**|**DATETIME**|**TIMESTAMP**|
|---|---|---|
|Laika zona|**Neatkarīgs** no laika zonas|**Atkarīgs** no laika zonas (automātiski pielāgojas)|
|Saglabātais formāts|Precīzs, kā ievadīts (nemainās)|Pārrēķina uz UTC un atkarībā no zonas rādās citādi|
|Diapazons|`1000-01-01` līdz `9999-12-31`|`1970-01-01` līdz `2038-01-19`|
|Lietošanas piemērotība|Ilgtermiņa dati (piemēram, dzimšanas datumi, vēsture)|Notikumu pieraksts, žurnāli, izveides laiki|
|Atmiņas patēriņš|8 baiti|4 baiti|

#### Vērtību ievades iespējas

`DATE`, `DATETIME` un `TIMESTAMP` atbalsta dažādus ievades formātus:

| **Formāts**           | **Piemērs**             | **Rezultāts MySQL**   |
| --------------------- | ----------------------- | --------------------- |
| `YYYY-MM-DD HH:MM:SS` | `"2022-06-16 16:37:23"` | `2022-06-16 16:37:23` |
| `YY.MM.DD H+M+S`      | `"22.05.31 8+15+04"`    | `2022-05-31 08:15:04` |
| `YYYY/MM/DD H*M*S`    | `"2014/02/22 16*37*22"` | `2014-02-22 16:37:22` |
| Bez atdalītājiem      | `"20220616163723"`      | `2022-06-16 16:37:23` |
| Tikai datums          | `"2021-02-12"`          | `2021-02-12 00:00:00` |
Datumu ieraksta piemērs:

```sql
CREATE TABLE date_table (datetime TIMESTAMP);
INSERT INTO date_table VALUES("2022-06-16 16:37:23");
INSERT INTO date_table VALUES("22.05.31 8+15+04");
INSERT INTO date_table VALUES("2014/02/22 16*37*22");
INSERT INTO date_table VALUES("20220616163723");
INSERT INTO date_table VALUES("2021-02-12");
SELECT * FROM date_table;
```

Laika zonas iestatīšanas piemērs:

```sql
CREATE TABLE timestamp_table (timestamp_field TIMESTAMP);
SET @@session.time_zone="+00:00"; -- сбрасываем часовой пояс в MYSQL
INSERT INTO timestamp_table VALUES("2022-06-16 16:37:23");
SET @@session.time_zone="+03:00"; -- меняем часовой пояс в MYSQL
SELECT * FROM timestamp_table;
```


---
### ⇄ Saistības
Avots >>> [Дата и время — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/datetime-data-type)
Iepriekšēja lapa >>> [[Ciparu datu tips]]
Nākama lapa >>> [[VIEW]]
___