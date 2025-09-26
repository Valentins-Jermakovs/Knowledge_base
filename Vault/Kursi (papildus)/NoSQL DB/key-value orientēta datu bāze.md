⏲ **Datums:** 2025-05-04   
⏲ **Laiks:** 11:36 
❚ **Tagi:**  #NoSQL 

⌬ **Objekts:**  `NoSQL`

---
### ⬢ Detalizēts apraksts
#### Darba uzsākšana

<mark style="background: #FF5582A6;">Svarīgi! Šī datu bāze darbojas tikai Firefox pārlūkā!</mark>

> Kā arī, pirms darba uzsākšanas izveido tokenu! Tas būs nepieciešams turpmāk.

Vispirms nepieciešams izveidot jauno `keyspace`. Šajā piemērā tas ir `key`.

Kad atslēga tika inicializēta, pārej uz sadaļu `Connect` -> `Select a Method` -> `GraphQL API`. Pēc tam patin uz leju un apakšsadaļā `2. Create a table` nospied violeto linku `GraphQL Playground`. Tiks atvērta grafiskā saskarne.

![[Pasted image 20250504114825.png]]

Pirmais ko ir jāizdara, pievieno savu iepriekš uzģenerēto tokenu:

![[Pasted image 20250504115129.png]]

Pēc tokena ievades spied pogu `Play`, sistēmai jāparāda visi tavi izveidotie `keyspace`:

![[Pasted image 20250504115242.png]]

> Sānu panelis `DOCS` ļauj apskatīt dokumentāciju un instrukciju, kā ko veidot. `!` zīme parāda, kā lauks ir obligāts aizpildei.
#### Tabulas izveide
Sākumā izdzēšam visu, kas ir rakstīts ievades laukā.

Pirmais mēs koda ievades laukā ievadām:

- `mutation{}` - apzīmējot ka mēs strādāsim ar šo grupu;
- `createTable()` - izmantosim šo komandu un iekavās ievadīsim argumentus lai izveidotu tabulu;
- `keyspaceName` - teksta mainīgais, kurā `keyspace` mēs vēlamies izveidot jauno tabulu, piemēra ietvaros tas ir `key` `keyspace` ko izveidojām iepriekš;
- `tableName ` - teksta mainīgais, kur mēs ierakstām kādu nosaukumu mēs vēlamies iedot jaunajai tabulai;
- `partitionKeys` - masīvs no partīciju atslēgām.

![[Pasted image 20250504120008.png]]

Izveidotas tabulas piemērs:

![[Pasted image 20250504121328.png]]

Tā iekļauj sevī: nosaukumu, partīcijas atslēgu, klasteru atslēgas un vērtības (tabulas kolonnas).

Pēc datu ievades, lai izveidot tabulu, spied pogu `Play`.
#### Darbs ar tabulu - sākums

Pārslēdzies uz cilni `graphql`.
Šo te URL adresi vajag mainīt:

```
[b0398dff-68f6-461c-866b-8847386b5b85-eu-west-1.apps.astra.datastax.com/api/graphql/system](https://b0398dff-68f6-461c-866b-8847386b5b85-eu-west-1.apps.astra.datastax.com/api/graphql/system)
```

Uz savu URL, tas ir, norādīt savu `keyspace`.

```
[b0398dff-68f6-461c-866b-8847386b5b85-eu-west-1.apps.astra.datastax.com/api/graphql/key](https://b0398dff-68f6-461c-866b-8847386b5b85-eu-west-1.apps.astra.datastax.com/api/graphql/key)
```

Pēc tabulas izveides sistēma automātiski mums uzģenerēs nepieciešams metodes, tas var apskatīt cilnē `DOCS`.
#### Darbs ar tabulu - ierakstu pievienošana tabulai

Izmantojam mums uzģenerēto insert metodi un veicam ierakstu tabulā:

![[Pasted image 20250504123450.png]]

Ja viss veiksmīgi izpildās, redzēsim šādu izvadu:

![[Pasted image 20250504122740.png]]

Rinda `insertshop()` atbilst par ierakstu tabulā un kādi lauki tiks aizpildīti.
Rinda `value{}` atbilst par to, kas tiks parādīts pēc pogas `Play` nospiešanas.
#### Apskatīt visu tabulas saturu

Lai to izdarīt, pielieto šādu sintaksi:

![[Pasted image 20250504123226.png]]
 
 Šādi viss izskatīsies, ja pieprasījums tiks izpildīts veiksmīgi: 
 ![[Pasted image 20250504123316.png]]
 
 Tas parādīs visus ierakstus tabulā, piemērā ir tikai viens ieraksts pavisam.
#### Ieraksta meklēšana pēc `Partition key`

Lai atrast konkrētu ierakstu pēc `Partition key`, izmanto šādu sintaksi:

![[Pasted image 20250504123932.png]]

`item` šajā gadījumā ir mainīgais, kurā  tiek saglabāt pieprasījums, to vari nosaukt kā gribi.
Rezultātā tiks iegūts šāds te izvads:

![[Pasted image 20250504124043.png]]
#### Datu modifikācija

Kā iepriekš izskatītā dokumentu orientētā datu bāzē, šeit arī nepastāv tādas iespējas viena lauka modifikācijai, ja nepieciešams mainīt kādu ierakstu, tad tas tiks mainīts pilnībā. Lai mainīt datus kāda ierakstā, vispirms, nepieciešama tā `Partition key`, un tad aizpildīt laukus ar jauniem datiem.

![[Pasted image 20250504125033.png]]

Pēc veiksmīgas datu modifikācijas tiks iegūts šāds izvads:

![[Pasted image 20250504125103.png]]
#### Tabulas filtrēšana - indeksācijas pieslēgšana

Pats `GrapQL` indeksāciju normāli neatbalsta, lai to ieviest tabulā, nepieciešams atgriezties uz `DataStax` galveno lapu un pāriet sadaļā `CQL Console`. No turienes pieslēgties pie vajadzīga `keyspace` un izmantojot šādu komandu:
`CREATE INDEX ON tabulas_nosaukums(lauka_nosaukums);`
pieslēgt indeksāciju vajadzīgam laukam. Turpmāk šo lauku ar indeksāciju varēs izmantot filtrēšanai.

Šādi apmēram tas izskatīsies konsolē:

![[Pasted image 20250504130059.png]]

Pēc indeksācijas pieslēgšanas dodamies atpakaļ uz `GrapQL` un izmantojot šādu sintaksi, filtrējam mums vajadzīgos datus:

![[Pasted image 20250504130409.png]]

Izvads izskatīsies apmēram šādi:

![[Pasted image 20250504130432.png]]

Lai filtrētu vairākus laukus, mums nepieciešams papildus laukiem pieslēgt indeksāciju, kā tas bija aprakstīts iepriekš. Apmēram šādi izskatīsies sintakse `GrapQL`:

![[Pasted image 20250504130643.png]]

Filtru tabula

|Predikāts|Skaidrojums|
|---|---|
|`eq`|ekvivalents, vienāds|
|`ne`|nav vienāds ar|
|`in`|sarakstā ir vērtība (…)|
|`nin`|sarakstā nav vērtības (….)|
|`gt`|lielāks|
|`lt`|mazāks|
|`gte`|lielāks vai vienāds|
|`lte`|mazāks vai vienāds|
|`exists`|pārbauda vei esksistē vērtība|
#### P.S.
<mark style="background: #ABF7F7A6;">Laiku pa laikam tevi var izmest no servera, vienkārši pārlādē lapu, pa jaunam ielīmē savu tokenu un maini URL.</mark>

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Navigācija - NoSQL DB]]
Nākama lapa >>> [[API pieslēgšana key-value DB]]

---