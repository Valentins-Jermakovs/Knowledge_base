⏲ **Datums:** 2025-05-09   
⏲ **Laiks:** 11:10 

❚ **Tagi:**  #NoSQL 
⌬ **Objekts:**  `NoSQL`

---
### ⬢ Detalizēts apraksts
#### Cypher deklaratīva vaicājumu valoda

| Vaicājums     | Skaidrojums                                                              |
| ------------- | ------------------------------------------------------------------------ |
| MATCH         | Izmanto, lai atrastu mezglus un malas datubāzē. Līdzīgi kā SQL 'SELECT'. |
| CREATE        | Izmanto, lai izveidotu jaunus mezglus un malas grafā                     |
| RETURN        | Norāda, kādu informāciju vaicājuma rezultātā jāatgriež.                  |
| WHERE         | Filtrē rezultātus, pamatojoties uz noteiktiem nosacījumiem.              |
| SET           | Atjaunina esošu mezglu vai attiecību īpašības.                           |
| DELETE        | Dzēš attiecības vai mezglus (ja nav saistītu attiecību).                 |
| DETACH DELETE | Dzēš mezglu kopā ar visām tā attiecībām.                                 |
| ORDER BY      | Sakārto rezultātus pēc noteikta lauka augošā vai dilstošā secībā.        |
| LIMIT         | Ierobežo rezultātu skaitu.                                               |
| COLLECT       | Apvieno vairākus rezultātus vienā                                        |
| COUNT         | Saskaita, cik daudz rezultātu ir.                                        |
| DISTINCT      | Izslēdz dublikātus no rezultātiem.                                       |
| STARTS WITH   | Nosaka, vai teksta lauks sākas ar konkrētu virkni.                       |
| CREATE INDEX  | Izveido indeksu īpašību meklēšanas veiktspējas uzlabošanai.              |
#### Mezgla izveide

Lai izveidot vienu objektu/mezglu, izmanto šādu sintaksi:
`CREATE (laurence:Actor {name: 'Laurence Fishburne'})`

Kur:

- `laurence` ir mainīgais, kurā tiek saglabāts objekts, tas nav obligāts;
- `:Actor` kategorija, pie kuras pieder objekts;
- `{}` objekta parametri, nosaukums, datumi, gadi utt.

Šāda loģika tiek izmanto priekš visa veida objektiem.
#### Mezgla modifikācija

Lai pievienot papildus parametru pie kāda objekta/mezgla, izmanto šādu sintaksi:
`MATCH (m:Movie {title: 'Mana filma'})
`SET m.genra = 'Sci-fi'`
`RETURN m`

Kur:
- `MATCH` nozīmē to pašu, ko `SELECT`, tas ir, izvilkt/atrast un tālāk iet parametri, kur `m:Movie` ir mainīgais un objekta kategorija, `{}` objekta parametri, pēc kuriem meklēt objektu kategorijā.
- `SET` nozīmē veikt modifikāciju, kur `m.genra` ir mainīgais un pievieno lauku `genra` ar vērtību `Sci-Fi`
- `RETURN m` atgriež mainīgo, lai varētu redzēt to.

Pievienot personas dzimšanas vietu:
`MATCH (p:Person {name: "Jānis Bērziņš"})`
`SET p.birthPlace = "Rīga"`
`RETURN p`
#### Attiecības

Objektu izveidei ar attiecībām starp tiem (sintakses piemērs):
`CREATE (m:Movie {title: "Jauna Filma", released: 2024, tagline: "Latvijas kinematogrāfija"})`
`CREATE (p:Person {name: "Jānis Bērziņš", born: 1980})`
`CREATE (p)-[:ACTED_IN]->(m)`

**Skaidrojums:**

- `(:Movie {...})` definē filmu ar īpašībām;
- `(:Person {...})` definē personu;
- `[:ACTED_IN]` attiecība starp personu un filmu.

**Atrast visas filmas, kurās spēlējis konkrēts aktieris:**
`MATCH (p:Person {name: "Tom Hanks"})-[:ACTED_IN]->(m:Movie)`
`RETURN m.title`

**Atrast režisorus noteiktai filmai:**
`MATCH (p:Person)-[:DIRECTED]->(m:Movie {title: "The Matrix"})`
`RETURN p.name`
#### Filtrs WHERE

Filtrs, kur izlaišanas datums lielāks par 2000 (sintakses piemērs):
`MATCH (m:Movie)`
`WHERE m.released > 2000`
`RETURN m.title, m.released`

Kur:

- `MATCH` nozīmē atrast objektu pēc tā kategorijas, parametriem;
- `WHERE` filtrs, šeit, filmas, kas tika izdotas pēc 2000. gada;
- `RETURN m.title, m.released` atgriež atlasīto filmu nosaukumus un izlaišanas datumus.

Filtrs, kur nosaukums sākas ar `The` (sintakses piemērs):
`MATCH (m:Movie)`
`WHERE m.title STARTS WITH "The"`
`RETURN m.title`
#### Dzēšana DELETE & DETACH DELETE

**Dzēst tikai attiecības:**
`MATCH (p:Person {name: "Jānis Bērziņš"})-[r:ACTED_IN]->(m:Movie {title: "Jauna Filma"})`
`DELETE r`

**Dzēst mezglu (ar visām attiecībām):**
`MATCH (m:Movie {title: "Jauna Filma"})`
`DETACH DELETE m`

**Visas DB dzēšana**
`MATCH (n)`
`DETACH DELETE n`
#### Sakārtošana un ierobežošana ORDER BY & LIMIT

`MATCH (m:Movie)`
`RETURN m.title, m.released`
`ORDER BY m.released DESC`
`LIMIT 5`

Kur:

- `ORDER BY` nosaka kārtošanas veidu;
- `LIMIT` nosaka, cik rezultātu izvadīt.
#### Sarežģītāku vaicājumu veikšana

Aktieri, kas spēlējuši kopā ar Tomu Henksu:
`MATCH (a:Person)-[:ACTED_IN]->(m:Movie)<-[:ACTED_IN]-(coactor:Person)`
`WHERE a.name = "Tom Hanks" AND coactor.name <> "Tom Hanks"`
`RETURN DISTINCT coactor.name`

Rinda `MATCH (a:Person)-[:ACTED_IN]->(m:Movie)<-[:ACTED_IN]-(coactor:Person)` meklē aktierus un co-aktierus, kuri spēlēja vienā filmā.

Rinda `WHERE a.name = "Tom Hanks" AND coactor.name <> "Tom Hanks"` filtrē `a` (objektus), kur aktieris bija Tom Hanks, bet co-aktieri nebija Tom Hanks.

Rinda `RETURN DISTINCT coactor.name` atgriež visus co-aktierus <mark style="background: #FFB86CA6;">bez atkārtojuma.</mark>
#### Agregātvaicājumi  COUNT, AVG, COLLECTION

**Cik filmu katrs režisors ir režisējis:**
`MATCH (p:Person)-[:DIRECTED]->(m:Movie)`
`RETURN p.name, COUNT(m) AS numMovies`
`ORDER BY numMovies DESC`

Rinda `RETURN p.name, COUNT(m) AS numMovies` atgriezīs režisorus ar filmu skaitu.

**Apkopot filmu nosaukumus vienam aktierim:**
`MATCH (p:Person {name: "Tom Hanks"})-[:ACTED_IN]->(m:Movie)`
`RETURN p.name, COLLECT(m.title) AS movies`

Rinda `RETURN p.name, COLLECT(m.title) AS movies` atgriezīs sarakstu (masīvu).

Atrast **vidējo filmu gadu**, ko režisējis katrs režisors:
```cypher
MATCH (d:Director)-[:DIRECTED]->(m:Movie)
RETURN d.name, AVG(m.year) AS avgYear
ORDER BY avgYear
```

Kas notiek:

- `MATCH`: atrodam režisoru un viņa režisētās filmas;
- `AVG(m.year)`: aprēķina vidējo gadu no visām šī režisora filmām;
- `RETURN`: parāda režisora vārdu un vidējo gadu;
- `ORDER BY`: sakārto rezultātu pēc vidējā gada (pēc izvēles).
#### Indeksēšana

Lai uzlabotu vaicājumu veiktspēju, var izveidot indeksus:
`CREATE INDEX FOR (p:Person) ON (p.name)`
`CREATE INDEX FOR (m:Movie) ON (m.title)`

---
### ⚛ Secinājums/i

Biežāk sastopami salīdzināšanas vaicājumi

| Vaicājums                              | Skaidrojums                                                                    |
| -------------------------------------- | ------------------------------------------------------------------------------ |
| `WHERE m.released = 1999`              | Atlasīt tikai tās filmas, kuras iznāca **1999. gadā**.                         |
| `WHERE p.name <> "Tom Hanks"`          | Izslēgt **Toma Henkša** ierakstu no rezultāta.                                 |
| `WHERE m.year > 2000`                  | Filtrēt filmas, kas iznāca **pēc 2000. gada**.                                 |
| `WHERE m.rating <= 7.5`                | Filtrēt filmas ar vērtējumu **līdz 7.5** (ieskaitot).                          |
| `WHERE p.age >= 30`                    | Izvēlēties personas, kuru vecums ir **vismaz 30 gadi**.                        |
| `WHERE m.title STARTS WITH "The"`      | Atlasīt filmas, kuru nosaukums **sākas ar "The"**.                             |
| `WHERE m.title CONTAINS "Matrix"`      | Atlasīt filmas, kuru nosaukumā **ir vārds "Matrix"** jebkurā pozīcijā.         |
| `WHERE m.genre IN ['Action','Sci‑Fi']` | Filtrēt filmas ar žanru **Action** vai **Sci‑Fi**, ja žanri glabāti kā masīvs. |

Loģiskie operatori Cypher

| Operators | Nosaukums     | Piemērs sintaksē                                   | Skaidrojums                                           |
| --------- | ------------- | -------------------------------------------------- | ----------------------------------------------------- |
| `=`       | vienāds       | `WHERE m.year = 1999`                              | Atlasa precīzi **1999. gadā** izdotos ierakstus.      |
| `<>`      | nav vienāds   | `WHERE p.name <> 'Neo'`                            | Izslēdz ierakstus, kur nosaukums ir **"Neo"**.        |
| `>`       | lielāks       | `WHERE p.age > 40`                                 | Atlasa personas ar vecumu **virs 40 gadiem**.         |
| `<`       | mazāks        | `WHERE m.rating < 8`                               | Filtrē filmas ar vērtējumu **zem 8**.                 |
| `>=`      | lielāks vai = | `WHERE m.year >= 2010`                             | Atlasa filmas, iznākušas **2010. gadā vai vēlāk**.    |
| `<=`      | mazāks vai =  | `WHERE p.age <= 25`                                | Izvēlas personas ar vecumu **līdz 25 gadiem**.        |
| `AND`     | un            | `WHERE p.age > 30 AND p.country = 'LV'`            | Apvieno divus nosacījumus — abiem jābūt patiesiem.    |
| `OR`      | vai           | `WHERE m.genre = 'Action' OR m.genre = 'Thriller'` | Atlasīt, ja **kaut viens** nosacījums izpildās.       |
| `NOT`     | nē / ne       | `WHERE NOT m.title STARTS WITH 'The'`              | Izslēdz ierakstus, kas **sākas ar "The"**.            |
| `IN`      | masīvā        | `WHERE m.genre IN ['Action','Sci‑Fi']`             | Pārbauda, vai vērtība ir **kādas no dotajām** masīvā. |

Kārtošanas veidi

| Sintakse              | Skaidrojums                                      |
| --------------------- | ------------------------------------------------ |
| `ORDER BY field ASC`  | Kārto **augošā** secībā (no mazākā uz lielāko)   |
| `ORDER BY field DESC` | Kārto **dilstošā** secībā (no lielākā uz mazāko) |
| `ORDER BY field`      | Noklusēti kārto **augošā** secībā                |
| `ORDER BY x, y DESC`  | Kārto pēc `x`, un tad pēc `y` (pēc vajadzības)   |

Kārtot filmas pēc iznākšanas gada (augoši):

```cypher
MATCH (m:Movie)
RETURN m.title, m.released
ORDER BY m.released
```

Kārtot pēc vārda dilstoši:

```cypher
MATCH (p:Person)
RETURN p.name
ORDER BY p.name DESC
```

Kārtot vispirms pēc gada, tad pēc nosaukuma:

```cypher
MATCH (m:Movie)
RETURN m.released, m.title
ORDER BY m.released DESC, m.title ASC
```

Top 3 aktīvākie režisori:

```cypher
MATCH (d:Director)-[:DIRECTED]->(m:Movie)
RETURN d.name, COUNT(m) AS moviesDirected
ORDER BY moviesDirected DESC
LIMIT 3
```

Interesants piemērs
**Uzdevums:** Atrod visus aktierus, kas ir **vecāki par 35 gadiem**, kuri **spēlējuši filmās** ar žanru **Sci‑Fi** un **nespēlējuši** nevienā **thriller** žanra filmā.

```cypher
MATCH (a:Actor)-[:ACTED_IN]->(m:Movie)-[:HAS_GENRE]->(g:Genre)
WHERE a.age > 35
  AND g.name = 'Sci‑Fi'
  AND NOT EXISTS {
    MATCH (a)-[:ACTED_IN]->(thr:Movie)-[:HAS_GENRE]->(:Genre {name: 'Thriller'})
  }
RETURN DISTINCT a.name, a.age
ORDER BY a.age DESC
```

- **`g.name = 'Sci‑Fi'`** - tikai Sci‑Fi žanra filmas;
- **`NOT EXISTS { … }`** - pārliecināmies, ka **nav nevienas** saites ar thriller žanra filmu;
- **`DISTINCT`** - nodrošina, ka katrs aktieris tiek atgriezts tikai vienreiz.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - NoSQL DB]]
Nākama lapa >>> [[API pieslēgšana grafu DB]]

---