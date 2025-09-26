⏲ **Datums:** 2025-05-02   
⏲ **Laiks:** 16:02 

❚ **Tagi:**  #NoSQL 
⌬ **Objekts:**  `NoSQL`

---
### ⬢ Detalizēts apraksts
#### Tabulu komandas
|Komanda|Piemērs|Apraksts|
|---|---|---|
|`CREATE TABLE`|`CREATE TABLE table_name (column_name UUID PRIMARY KEY, column_name text, column_name text, column_name timestamp);`|Izveido jaunu tabulu ar kolonnām un primāro atslēgu.|
|`ALTER TABLE ADD`|`ALTER TABLE table_name ADD column_name int;`|Pievieno jaunu kolonnu esošai tabulai.|
|`ALTER TABLE ALTER`|`ALTER TABLE table_name ALTER column_name TYPE datatype;`|Maina esošas kolonnas datu tipu.|
|`ALTER TABLE WITH`|`ALTER TABLE table_name WITH caching = {'keys' : 'NONE', 'rows_per_partition' : '1'};`|Maina tabulas īpašības, piemēram, kešošanas iestatījumus.|
|`DROP TABLE`|`DROP TABLE table_name;`|Izdzēš tabulu no datu bāzes.|
|`TRUNCATE`|`TRUNCATE table_name;`|Dzēš visus datus tabulā, bet patur tabulas definīciju.|

#### Salīdzināšanas operatori

Šie operatori tiek lietoti `WHERE` klauzulā, lai filtrētu vaicājuma rezultātus:

- `=` vienāds;
- `!=`  nav vienāds;
- `>` lielāks par;
- `>=` lielāks vai vienāds ar;
- `<` mazāks par;
- `<=` mazāks vai vienāds ar;
- `IN` pieder kādai vērtību kopai;
- `CONTAINS` satur doto vērtību kolekcijā;
- `CONTAINS KEY` satur doto atslēgu `map` tipa kolonnā.
#### Datu meklēšana ārpus `Partition key`

Lai veiktu meklēšanu tabulas kolonnās, kas nav definētas kā partīcijas vai klasteru atslēgas, var izmantot šādu komandu:
`SELECT * FROM tabulas_nosaukums WHERE kolonnas_nosaukums = vērtība ALLOW FILTERING;`

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Tabulāra, kolonnu orientēta datu bāze ar klasterizāciju]]
Nākama lapa >>> [[API tabulāra DB]]

---