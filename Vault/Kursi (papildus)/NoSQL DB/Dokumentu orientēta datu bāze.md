⏲ **Datums:** 2025-05-03   
⏲ **Laiks:** 10:01 
❚ **Tagi:**  #NoSQL 

⌬ **Objekts:**  `NoSQL`

---
### ⬢ Detalizēts apraksts
#### Darba uzsākšana

Sākumā ir jāizveido jauno `keyspace`, aprakstītā piemērā tas ir `document`.
Pēc `keyspace` izveides vajag pāriet `Setting` -> `Tokens`, ģenerēt tokenu, `Role` iestati uz `Administrator User`. Pēc tokena ģenerācijas, ielādē tokena failu uz datora un nospied `Back to portal`.

Tālāk -> `Connect`, izvēlies metodi `Document API` un zem `Launch Swagger UI` nospied violeto linku.
#### Kolekcijas izveide

Sadaļa `Collection` -> `Create a collection`.
Pie `namespace` ievadi savu `keyspace`, piemērā tas ir `document`.
Pie `name` uzraksti savas kolekcijas nosaukumu. Skat. attēlu:

![[Pasted image 20250503101402.png]]

Pēc visas datu ievades spied `Execute`.
#### Dokumenta izveide

Sadaļa `Documents` -> `Create a document`.
Pie `namespace` ievadi savu `keyspace`.
Pie `collection` ievadi savas kolekcijas nosaukumu.

![[Pasted image 20250503102557.png]]

Pēc visu vajadzīgo datu ievades poga `Execute`.

P.S. Ieteicams kaut kur ārpus saglabāt dokumenta id, kas tiks parādīts uzreiz, pēc tā izveidošanas, var noderēt turpmāk:

![[Pasted image 20250503102729.png]]
#### Visu dokumentu apskats kolekcijā

Lai apskatīt visus dokumentus, kas ir kolekcijā, sadaļa `Documents` -> `Searc documents in collection`. Ievadi `keyspace` un kolekcijas nosaukumu. Nospied pogu `Execute`.

![[Pasted image 20250503103756.png]]
#### Dokumenta meklēšana pēc tā vērtībām

Lai veikt filtrāciju, ieteicams izmantot šo tabulu:

| Predikāts | Skaidrojums              |
| --------- | ------------------------ |
| $eq       | Equal to                 |
| $ne       | Not equal to             |
| $in       | In                       |
| $nin      | Not in                   |
| $gt       | Greater than             |
| $lt       | Less than                |
| $gte      | Greater than or equal to |
| $lte      | Less than or equal to    |
| $exists   | Exists                   |

Meklēšana notiek sadaļā `Documents` -> `Searc documents in collection`. Atšķirība tāda, kā tiek ievadīts filtrs laukā `where(query)`.

![[Pasted image 20250503104644.png]]

Izkrītošais saraksts `Examples` piedāvā sintakses piemērus. Pēc filtru ievades poga `Execute`.

![[Pasted image 20250503104755.png]]

Sintakses piemēru tabula:

| Izteiksme                                           | Apraksts latviešu valodā                                         |
| --------------------------------------------------- | ---------------------------------------------------------------- |
| `"age": { "$eq": 30 }`                              | Vecums ir vienāds ar 30                                          |
| `"status": { "$ne": "inactive" }`                   | Statuss nav "inactive"                                           |
| `"category": { "$in": ["electronics", "books"] }`   | Kategorija ir viena no: "electronics", "books"                   |
| `"category": { "$nin": ["furniture", "clothing"] }` | Kategorija nav neviena no: "furniture", "clothing"               |
| `"price": { "$gt": 100 }`                           | Cena ir lielāka par 100                                          |
| `"price": { "$lt": 50 }`                            | Cena ir mazāka par 50                                            |
| `"quantity": { "$gte": 10 }`                        | Daudzums ir lielāks vai vienāds ar 10                            |
| `"quantity": { "$lte": 5 }`                         | Daudzums ir mazāks vai vienāds ar 5                              |
| `"email": { "$exists": true }`                      | E-pasta lauks eksistē                                            |
| `"array_two": { "$elemMatch": { "$in": [5, 8] } }`  | Masīvā `array_two` ir vismaz viens elements, kas atbilst 5 vai 8 |
#### Dokumenta modifikācija

Sadaļa `Document` -> `Create or update a document`.
Ievadi `kyespace`, kolekcijas nosaukumu un dokumenta id un jauno saturu.

<mark style="background: #FF5582A6;">Atceries! Šī lauka vērtības pilnībā aizstās dokumenta saturu! Tas nozīmē, ja gribi veikt sadaļu tikai kādam konkrētam laukam, tev jāparaksta viss dokuments un jāpamaina vērtību tikai vajadzīgam laukam.</mark>

![[Pasted image 20250503105338.png]]

Poga `Execute`, lai apstiprināt izmaiņas.
#### Vairāku dokumentu izveide vienlaikus

Sadaļa `Document` -> `Create a documents`
Ievadi visus nepieciešamos datus, ko pieprasa sistēma. Zemāk parādīts piemērs ar vairāku dokumentu izveidi:

![[Pasted image 20250503105534.png]]
#### P.S.
Var gadīties kā dokumentu izveide vai meklēšana nedarbosies, lai to atrisināt, vajag autorizēties, izmantojot iepriekš ielādētu tokena failu.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - NoSQL DB]]
Nākama lapa >>> [[API pieslēgšana Dokumentu DB]]

---