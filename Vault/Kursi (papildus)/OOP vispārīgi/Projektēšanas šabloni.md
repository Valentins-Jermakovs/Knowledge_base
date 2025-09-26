⏲ **Datums:** 2025-05-22   
⏲ **Laiks:** 19:18 
❚ **Tagi:**  #OOP 

⌬ **Objekts:**  `OOP`

---
### ⬢ Detalizēts apraksts
#### Kas ir projektējamais šablons?
**Projektēšanas šabloni** ir īpašas struktūras objektorientētajā programmēšanā (OOP), kas palīdz risināt bieži sastopamas problēmas, veidojot sarežģītas programmas.

Katram projektēšanas šablonam ir:
- **Nosaukums** – izdomāts, lai varētu viegli runāt par konkrēto risinājumu;
- **Problēma** – situācija, kurā šis šablons var būt noderīgs;
- **Risinājums** – klašu struktūra (kā objekti ir izveidoti un sadarbojas), kas palīdz atrisināt problēmu;
- **Sekas (Apsvērumi)** – plusi un mīnusi, izmantojot šo šablonu konkrētā gadījumā.
#### Projektēšanas šabloni
Projektēšanas šabloni iedalās trīs galvenajās grupās:
- **Objektu veidošanas (creational) šabloni** – paredzēti objektu izveides procesa organizēšanai un pārvaldīšanai;
- **Strukturālie (structural) šabloni** – paredzēti dažādu klašu un objektu kombinēšanai, lai izveidotu lielākas struktūras;
- **Uzvedības (behavioral) šabloni** – paredzēti klašu un objektu mijiedarbības un uzvedības kontrolei programmas darbības laikā.
#### Builder
**Builder** šablonu izmanto, ja konstruktors satur pārāk daudz parametru un katrs objekts ir unikāls. Šādā gadījumā visu parametru vienlaicīga norādīšana nav ērta, tāpēc tiek izmantots pakāpenisks objekta veidošanas process.

**Prototype** šablona raksturīga iezīme ir tāda, ka objekta īpašības tiek iestatītas, izmantojot metodes, piemēram, `setProperty(param)` vai `AddParameter()`.

**Lietošanas gadījumi:**
- lietotāja saskarnes elementu stilizācija;
- klases ar daudzām īpašībām (laukumiem);
- situācijas, kad lietotājam jāspēj konfigurēt katru īpašību atsevišķi.

![[Pasted image 20250522194409.png]]
#### Builder 2
Lai nebūtu nepieciešams katru parametru iestatīt jaunā rindā, bieži vien **Builder** metodes tiek veidotas tā, lai tās atgrieztu pašu **Builder** objektu, izmantojot `this`. Tādējādi īpašības var iestatīt ķēdes (chain) veidā – vienā izsaukumu virknē.

**Lietošanas gadījumi:**
- ērti, ja nepieciešams rediģēt tikai dažus parametrus, nevis visus.

![[Pasted image 20250522194630.png]]

#### Director of Builder
**Director** tiek izmantots kopā ar **Builder** šablonu. **Director** ir atbildīgs par objektu veidošanas procesa vadību un piedāvā iepriekš definētas īpašību kombinācijas.

**Lietošanas gadījumi:**
- ērti, ja ir pieejami gatavi kombināciju šabloni;
- piemērots gadījumos, kad lietotājs nevar izveidot savas pielāgotas kombinācijas, bet var izvēlēties kādu no iepriekš sagatavotajiem variantiem.

![[Pasted image 20250522194908.png]]

#### Prototype
**Prototype** šablons ļauj izveidot vairākus objektus kā kopijas no iepriekš konfigurēta objekta.

Šī šablona galvenā iezīme ir tāda, ka klase spēj sagatavot objektu un pēc tam veidot tā kopijas, izmantojot metodi **`Clone()`**.

**Lietošanas gadījumi:**
- kad objektu dati lielākoties ir vienādi, un mainās tikai daļa no vērtībām;
- ja lietotājs var izveidot savu dizainu vai konfigurāciju, kuru nepieciešams kopēt vairākas reizes;
- kad jāveido vairāki līdzīgi ieraksti, piemēram, personalizēti pasūtījumi.

![[Pasted image 20250522200101.png]]
#### Singleton
**Singleton** ir neatņemama struktūra situācijās, kad programmēšanas valoda neatbalsta globālus mainīgos. Tas nodrošina, ka visā projektā tiek izveidots tikai viens objekts.

Šī šablona raksturīgā iezīme ir tāda, ka klase nepieļauj vairāku objektu izveidi, bet caur metodi **`getInstance()`** atgriež vienīgo esošo objektu. Konstruktors ir **private**, tāpēc to nevar izsaukt tieši no ārpuses.

**Lietošanas gadījumi:**
- lietotāja datu glabāšanai;
- pagaidu faila apstrādes kopijas uzturēšanai;
- sistēmas konfigurācijas pārvaldībai;
- koplietojamu resursu, piemēram, pogu ikonām vai bildēm, kas tiek izmantotas vairākās vietās.

![[Pasted image 20250522200733.png]]

![[Pasted image 20250522200747.png]]
#### Abstract Factory
**Abstract Factory** projektēšanas šablonu izmanto, kad nepieciešams radīt objektus vienādā stilā, bet dažādās grupās vai kategorijās.

![[Pasted image 20250522200956.png]]
#### Factory Method
**Factory Method** projektēšanas šablonu izmanto situācijās, kad programma atbalsta moduļus ar vienādiem pamatprincipiem, taču algoritmi un izmantotās klases var atšķirties.
![[Pasted image 20250522201238.png]]
#### Flyweight
**Flyweight** ir struktūras dekompozīcijas šablons, kas ļauj koplietot datus, kuri ir vienādi visiem objektiem, saglabājot tos atsevišķā kopīgā objektā. Tas palīdz samazināt atmiņas (RAM) patēriņu.

**Flyweight** šablona būtība ir tajā, ka mēs izveidojam **koplietojamu objektu,** kurā tiek glabāti **kopīgi dati**, kurus izmanto daudzi citi objekti vai klases.

**Lietošanas gadījumi:**
- nepieciešamība samazināt atmiņas patēriņu, īpaši, ja ir liels skaits līdzīgu objektu.

![[Pasted image 20250522202047.png]]
#### Boxing & Unboxing
**Boxing un Unboxing** nav klasiskā nozīmē projektēšanas šablons, bet gan programmēšanas tehnika, ko izmanto, kad nepieciešams nodot metodei dažādus datu tipus **bez metodes pārlādēšanas (overload)**.

**Boxing** nozīmē, ka **vērtību tipa** dati (piemēram, `int`, `bool`) tiek ietverti kā **objekti** (reference type), lai tos varētu apstrādāt kā vienotu tipu.  
**Unboxing** ir pretējais process — objekts tiek pārvērsts atpakaļ par konkrētu vērtību tipu.

**Lietošanas gadījumi:**
- datu tipu konvertēšana (piemēram, no `int` uz `object` un atpakaļ);
- vērtību **serializācija** un nosūtīšana pa tīklu vai glabāšana datnēs;
- kolekcijas, kurās glabājas dažāda tipa dati (piemēram, ziņojumu saraksti ar dažādiem datu formātiem).

![[Pasted image 20250523111636.png]]

![[Pasted image 20250523111703.png]]
#### Facade
**Facade** (strukturālais šablons) ir projektēšanas šablons, kas ļauj **paslēpt sarežģītu sistēmas uzbūvi**, piedāvājot vienkāršu un vienotu saskarni darbam ar vairākām iekšējām komponentēm.

**Raksturīgās iezīmes:**
- Facade slēpj vairākas aizmugures realizācijas, atstājot tikai nepieciešamās ievades un izvades;
- dažādas sistēmas daļas tiek izsauktas caur vienotu **interfeisu**;
- tas padara sistēmu vieglāk lietojamu un saprotamu no ārpuses.

**Lietošanas gadījumi:**
- optimāla funkcionalitātes izvēle atkarībā no ārējiem apstākļiem (piemēram, lietotāja ierīce, OS);
- dažādu sistēmas versiju atbalsts (piemēram, API v1, v2...);
- daudzvalodu atbalsts, kur valodas izvēle notiek caur vienotu mehānismu;
- datorspēlēs — dažādu spraitu (sprites) zīmēšana, paslēpjot sarežģīto grafikas infrastruktūru.

**Piezīme:** Izvēli starp apstrādes variantiem var veikt pats lietotājs, vai arī to var noteikt sistēma automātiski — piemēram, balstoties uz operētājsistēmu vai ierīces iestatījumiem.

![[Pasted image 20250523112117.png]]
#### Proxy
**Proxy** (strukturālais šablons) tiek izmantots, lai **kontrolētu piekļuvi pie citu klašu funkcionalitātes**, piemēram, resursietilpīgām metodēm vai ārējiem servisiem.

**Raksturīgās iezīmes:**
- Proxy darbojas kā **starpnieks** starp klientu un īsto objektu;
- tas var ierobežot, atlikt vai optimizēt piekļuvi pie galvenā objekta.

**Lietošanas gadījumi:**
- piekļuves kontrole konkrētai funkcionalitātei (piemēram, tikai autorizētiem lietotājiem);
- rezultātu **kešošana**, lai atkārtoti izmantotu jau aprēķinātus datus un samazinātu sistēmas noslodzi;
- piemēram: ja ārējs meteodatu serviss (API) atļauj tikai 2 pieprasījumus stundā, **proxy** var ierobežot pieprasījumus līdz vienam ik pēc 30 minūtēm un nodrošināt pārējiem objektiem jau saņemtos (iepriekšējus) datus.

![[up.png]]
#### Adapter
**Adapter** (strukturālais šablons) tiek izmantots, kad nepieciešams **izveidot savienojumu starp divām nesaistītām sistēmām vai komponentēm**, kuras **nav iespējams tieši modificēt**.

**Raksturīgās iezīmes:**
- Adapteris darbojas kā **tulks** starp divām nesaderīgām klasēm vai interfeisiem;
- tas ļauj vienai sistēmas daļai izmantot citas daļas funkcionalitāti, nemainot sākotnējo kodu.

**Lietošanas gadījumi:**
- ja sistēma pieprasa konkrētu interfeisu, bet esošajai klasei tas neatbilst;
- ja nepieciešams savienot dažādas datu struktūras, failu formātus vai ārējās bibliotēkas;
- ja tiek izmantots trešās puses risinājums, kura metodes vai funkcijas **nedrīkst mainīt**, bet jāpielāgo savas sistēmas vajadzībām.

![[edited.png]]
#### Iterator
**Iterator** ir projektēšanas šablons, kas ļauj **pakāpeniski pārstaigāt kolekciju (piemēram, sarakstu, koku, u.c.) bez nepieciešamības tieši izmantot indeksus**.

**Raksturīgās iezīmes:**
- klase satur kolekciju ar vērtībām;
- caur metodi **`getNext()`** tiek atgriezts nākamais neapstrādātais elements;
- process turpinās līdz brīdim, kad **`isDone()`** metode norāda, ka visi elementi ir apstrādāti.

**Lietošanas gadījumi:**
- **standarta risinājums masīvu un sarakstu apstrādei** Python un citās modernās valodās;
- attēlu apstrāde pikseli pēc pikseļa;
- ziņojumu rindas (FIFO – first-in, first-out) pārvaldība.

**Piezīme:** Nav obligāti jādefinē viss saraksts iepriekš – nākamais elements var tikt **dinamiski ģenerēts izsaukuma laikā**, piemēram, spēlēs, kur notikumi rodas reāllaikā.

![[Pasted image 20250523113752.png]]
#### Chain of Responsibility
**Chain of Responsibility** (atbildības ķēde) ir projektēšanas šablons, kas nodrošina **datu vai pieprasījuma apstrādi secīgu posmu veidā**. Katrs posms pats izlemj, vai apstrādāt pieprasījumu, vai nodot to tālāk nākamajam posmam ķēdē.

**Raksturīgās iezīmes:**
- katrs posms (mezgls) darbojas **neatkarīgi**, tāpēc tos var viegli **mainīt, pievienot vai izņemt**;
- ķēdes **secību var brīvi konfigurēt**, nepārveidojot visu sistēmu;
- uzlabota koda elastība un modularitāte.

**Lietošanas gadījumi:**
- **anketu, pirkumu vai konfigurāciju** apstrāde pa soļiem;
- **datu vai attēlu apstrāde** ar vairākiem filtriem vai pārveidotājiem;
- sistēmas, kur nepieciešams **viegli pielāgot soļu secību vai aizvietot posmus** (piemēram, validācija, autorizācija, transformācija).

![[edited2.png]]
#### State
**State** ir projektēšanas šablons, kas balstās uz **galīgiem stāvokļu automātiem (Finite-State Machine)** un tiek izmantots, lai aprakstītu objektu uzvedību atkarībā no to **iekšējā stāvokļa**.

**Raksturīgās iezīmes:**
- sistēmas uzvedība tiek modelēta kā **matemātisks grafiks**, kur **virsotnes** attēlo stāvokļus un **loki** — pārejas starp tiem;
- klase parasti satur divas galvenās metodes:
    - **`doTask()`** — izpilda konkrētā stāvokļa darbību;
    - **`nextState()`** — nosaka un aktivizē nākamo stāvokli.

**Lietošanas gadījumi:**
- **robotu vai automātisko sistēmu uzvedības modelēšana**, kur reakcija atkarīga no ārējiem faktoriem;
- sarežģītas **apstrādes ķēdes ar zarojumiem, nosacījumiem un pārejām starp dažādām situācijām**;
- piemērots gadījumiem, kur objekts **maina savu uzvedību dinamiski** atkarībā no konteksta.

**Piezīme:** Pirms realizācijas bieži **izstrādā matemātisko grafu**, kas apraksta visus iespējamos stāvokļus un pārejas starp tiem — tas nodrošina pārskatāmu loģiku un vieglu paplašināšanu.

![[Pasted image 20250523114939.png]]

![[Pasted image 20250523114739.png]]
#### Visitor
**Visitor** ir projektēšanas šablons, kas ļauj **definēt operācijas dažādiem objektu tipiem**, neieviešot šīs operācijas pašās datu klasēs. To izmanto, kad **polimorfisms nav iespējams** (piemēram, kad objekti nepieder vienai mantošanas hierarhijai vai mantošana ir aizliegta).

**Raksturīgās iezīmes:**
- loģika tiek izdalīta uz **atsevišķu Visitor klasi**, nevis glabājas datu klasēs;
- datu klase satur metodi, kas **pieņem Visitor objektu** un ļauj tam veikt apstrādi (piemēram, `accept(visitor)`).

**Lietošanas gadījumi:**
- **datu eksportēšana dažādos formātos**, piemēram, uz CSV, XML, JSON, kur katram formātam ir savs Visitor;
- jāapstrādā **dažāda tipa dati ar dažādu loģiku**, bet visu apvieno viens Visitor;
- situācijas, kur:
    - **katrs datu tips tiek apstrādāts atšķirīgi**;
    - **nav iespējas mainīt datu klašu kodu** vai izmantot mantošanu.

![[edited3.png]]

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Navigācija - OOP vispārīgi]]

---