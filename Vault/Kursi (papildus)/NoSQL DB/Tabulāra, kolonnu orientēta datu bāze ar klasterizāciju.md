⏲ **Datums:** 2025-05-02   
⏲ **Laiks:** 15:24 

❚ **Tagi:**  #NoSQL 
⌬ **Objekts:**  `NoSQL`

---
### ⬢ Detalizēts apraksts
#### Tabulas izveide ar vairākām klasteru atslēgām

Šajā piemēra tiek parādīts, kā izveidot tabulu ar vairākām atslēgām klasteru atslēgām:

![[Pasted image 20250502153639.png]]

Tiek veidota `Partition key`, kas netiek pievienota klasterim, tiek ierakstīta iekavās, šeit `(country)`, pārējas atslēgas aiz komata, `((country), name, url)`, kas ir klastera atslēgas.

Lai pieslēgt klasterizāciju, komanda `WITH CLUSTERING ORDER BY(name DESC, url ASC)`.
<mark style="background: #ABF7F7A6;">DESC: kārtot krītoša/dilstoša kārtība; ASC: kārtot augoša kārtība.</mark>
#### Ierakstu pievienošana

Šeit nekas nemainās, viss ir identiski kā  iepriekšējā rakstā >>> [[Tabulāra, kolonnu orientēta datu bāze bez klasterizācijas]]

![[Pasted image 20250502154559.png]]
#### Klasteris

Jā tabulā eksistēs divi ieraksti, kuriem sakrīt `Partition key`, to secība tiks kārtota atbilstoši klasterim.

![[Pasted image 20250502155009.png]]

---
### ⚛ Secinājums/i

Šajā piemērā parādīts, kā izveidot tabulu, kurā tiek izmantots viens **partition key** un vairākas **clustering kolonnas**:

```sql
CREATE TABLE restorounts (
    country text,
    name text,
    cuisine text,
    url text,
    PRIMARY KEY ((country), name, url)
) WITH CLUSTERING ORDER BY (name DESC, url ASC);
```

**Partition key** ir lauks, kas definē datu fizisko sadalījumu pa nodiem (nodes) klasterī. Šeit tas ir `country`, un tas tiek rakstīts iekavās: `((country), ...)`.
**Clustering columns** ir lauki, kas nosaka ierakstu kārtošanas secību **iekšpusē katrā partition.** Šeit tie ir `name` un `url`.

Komanda `WITH CLUSTERING ORDER BY (name DESC, url ASC)` nosaka, ka:
- ieraksti katrā partition tiks kārtoti vispirms pēc `name` dilstošā secībā (DESC);
- un, ja `name` ir vienādi — tad pēc `url` augošā secībā (ASC).

Datu ievietošana šajā tabulā notiek tāpat kā tabulās bez klasterizācijas, izmantojot `INSERT INTO`. Ja tabulā ir vairāki ieraksti ar vienādu `country`, tie tiks **saglabāti un iegūti** noteiktajā kārtošanas secībā atbilstoši `name` un `url` klasterizācijai.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Tabulāra, kolonnu orientēta datu bāze bez klasterizācijas]]
Nākama lapa >>> [[Cassandra CQL]]

---