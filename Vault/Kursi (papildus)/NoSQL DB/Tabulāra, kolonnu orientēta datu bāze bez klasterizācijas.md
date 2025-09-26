⏲ **Datums:** 2025-05-02   
⏲ **Laiks:** 14:13 

❚ **Tagi:**  #NoSQL
⌬ **Objekts:**  `NoSQL`

---
### ⬢ Detalizēts apraksts
#### Datu bāzes izveide

![[Pasted image 20250502141647.png]]

Pēc jaunās datu bāzes izveides vajag nedaudz uzgaidīt, lai tā tiktu inicializēta.

> Jā vajag izveidot jauno `keyspace` -> `add keyspace` un ievadi nosaukumu.
#### Tabulas izveide

Lai izveidot tabulu, no galvenā datu bāzes loga vajag doties uz -> `CQL Console`

![[Pasted image 20250502142416.png]]

Lai uzzināt, kādi `kyespace` ir pieejami sistēmā, ievadi komandu `DESCRIBE KEYSPACES;`

Tālākam darbam izmanto vienu no saviem `keyspace`
Lai to izmantot -> `USE your-keyspace;`

Lai izveidot tabulu, izmanto komandu `CREATE TABLE IF NOT EXISTS tabulas-nosaukums (`

![[Pasted image 20250502143303.png]]

Ja viss ir kārtībā, tabulai vajadzētu izveidoties.

> Šeit tika pielietota komanda `PRIMARY KEY (atslēgas-nosaukums)`
>Šī komanda ir nepieciešama, lai izveidot `Partition key`, pēc kuras tiks meklēti vajadzīgi
>ieraksti tabulā. Tabulārās/kolonnu datu bāzēs tas saucas par `Partition key`, SQL datu
>bāzēs (relāciju), tas saucas par `Primary key`.

Lai apskatīt izveidoto tabulu, izmanto komandu `SELECT * FROM tabulas-nosaukums;`

![[Pasted image 20250502144134.png]]
#### Ierakstu pievienošana tabulā

Lai veikt ierakstu, izmanto komandu `INSERT INTO tabulas-nosaukum (tabulas-lauki) VALUES (lauku-vērtības);`

![[Pasted image 20250502145054.png]]
#### Datu meklēšana pēc `Partition key`

Izmanto šādu komandu, lai izvadīt visus ieraksta laukus/kolonnas, kā `Partition key` vienāda ar tevis norādīto vērtību.
`SELECT * FROM tabulas-nosaukums WHERE atslēgas-nosaukums = vērtība;`

![[Pasted image 20250502150159.png]]
#### Jaunas kolonnas pievienošana eksistējošai tabulai

Lai pievienot jauno kolonnu jau eksistējošai tabulai, izmanto komandu:
`ALTER TABLE tabulas-nosaukums ADD jaunās-kolonnas-nosaukums kolonnas-datu-tips;`

![[Pasted image 20250502150853.png]]
#### Datu atjaunošana

Lai mainīt datus jau eksistējošā tabulas kolonnā vai jaun-pievienotajā kolonnā, izmanto šādu komandu:
`UPDATE tabulas-nosaukums SET kolonna = vērtība WHERE atslēga = vērtība;`

![[Pasted image 20250502151353.png]]

#### Datu iegūšana no jebkuras kolonnas

Izmanto `ALLOW FILTERING`, darbojas tikai ar `SELECT`.

```
SELECT * FROM banksystem WHERE sallary = 800 ALLOW FILTERING;
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - NoSQL DB]]
Nākama lapa >>> [[Tabulāra, kolonnu orientēta datu bāze ar klasterizāciju]]

---