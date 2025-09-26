⏲ **Datums:** 2025-05-03   
⏲ **Laiks:** 11:51 
❚ **Tagi:**  #OOP 
⌬ **Objekts:**  `OOP`

---
### ⬢ Detalizēts apraksts
#### Ievads

Programmēšanas valodās funkcija ir procedūra, kuras izpildes rezultātā
tiek formēta kāda vērtība un kuras izsaukums var tikt izmantots kā kādas
izteiksmes operands.

**Procedūra** - darbību secība, kas jāveic, lai atrisinātu kādu uzdevumu.
**Operands** - lielums izteiksmē, ar kuru izdara darbību.
#### Kas ir klase un objekts?

Klase ir datu un funkciju loģiskā grupa, kura attēlo kādu priekšmetu vai
vienību. Klasi vajag asociēt ar šablonu.

Objekts ir konkrēts klases eksemplārs - pārstāvis.

Klase sastāv no:

- nosaukuma;
- klases atribūtiem/laukiem (tās mainīgie);
- konstruktora jeb funkcijas, lai izveidotu klases eksemplāru (objektu).
#### Dekompozīcija

Dekompozīcija – tā ir pieeja, kad sarežģīta problēma tiek sadalīta
mazākos uzdevumos, kurus ir vienkāršāk risināt, saprast un ar kuriem ir
vienkāršāk strādāt.
#### UML

Unified Modeling Language (UML) ir notācija jeb „standarts“, kā vizuāli
aprakstīt sistēmu

UML specifikācijā ir aprakstītas šādas diagrammas:

- Sistēma-lietotājs (prasības): use case diagrammas;
- Sastāvdaļas-saites: pakešu diagrammas un klašu diagrammas;
- Procesi: aktivitāšu diagrammas, secību diagrammas, stāvokļu diagrammas.
#### Piekļuves specifikatori

Piekļuves specifikatori norāda,no kurienes ir pieejams klases elements:

- `-` = private: apzīmē slēptos klases elementus;
- `+` = public: apzīmē atklātos klases elementus;
- `#` = protected: apzīmē aizsargātos klases elementus.
#### Īpašības

Īpašības ir metodes, kuras:

- maina lauku vērtības (set);
- vai atgriež lauku vērtības (get).

Īpašības ir pieņemts saukt, sākot ar vārdiem `set` vai `get`.
#### Inkapsulācija

Inkapsulācija ir OOP pieeja, kad objekta iekšējā struktūra un iekšējie procesi tiek paslēpti.
Inkapsulācija tiek izveidota, pielietojot pieejas specifikatorus un īpašības. Piem., melnā kaste ar ievadiem un izvadiem, kas notiek kastē, neviens nezina.
#### Saites starp klasēm

**Asociācija** attēlo, ka starp diviem objektiem ir saite, bet paši objekti var būt arī nesaistīti.
**Salikums (composition)** apraksta situāciju, kad objekts sastāv no citiem objektiem, bez kuriem tas nevar eksistēt. Objekti-sastāvdaļas arī nevar eksistēt bez objekta, kuru tie veido.
**Apvienošana (aggregation)** aprakstā situāciju, kad objekts satur citu objektu, bet objekti var eksistēt atsevišķi.
#### Mantošana un polimorfisms

**Mantošana** ir saite, kad viena klase iemanto visas metodes un laukus no vecākklases/virsklases (parent class, superclass).
**Polimorfisms** ir īpašība, kad objekts var pieņemt virsklašu datutipus un strādāt, izmantojot virsklašu loģiku.
#### Interfeiss

C# valodā par interfeisu sauc speciālu klasi, kura tikai apraksta kādas metodes jāsatur klasēm, kuras manto šo interfeisu. Interfeisu ir pieņemts saukt, sākot ar lielu burtu 'I'.
#### Nosaukumvieta

Nosaukumvieta ir pieeja kā apvienot loģiski saistītas klases vienā kopā. Nosaukumvietas arī izmanto, lai atšķirtu divas klases ar vienādu nosaukumu.
#### `new` un `override`
##### `new`
**`new`** C# valodā nozīmē, ka tu **paslēpj** bāzes klases metodi ar jaunu metodi tajā pašā nosaukumā. Tas nav pārrakstījums, bet gan **aizstāšana**, kas darbojas tikai tad, ja objekts tiek lietots kā atvasinātās klases tips.

```cs
class Baze {
    public void Izvade() {
        Console.WriteLine("Bāze");
    }
}

class Atvasinata : Baze {
    public new void Izvade() {
        Console.WriteLine("Atvasināta (new)");
    }
}

class Program {
    static void Main() {
        Baze objekts1 = new Atvasinata(); // tips: Baze
        Atvasinata objekts2 = new Atvasinata(); // tips: Atvasinata

        objekts1.Izvade(); // -> "Bāze"
        objekts2.Izvade(); // -> "Atvasināta (new)"
    }
}
```
##### `override`

**`override`** nozīmē, ka tu **pārraksti** (pārdefinē) **virtuālu metodi** no bāzes klases, lai tā **strādātu arī tad, ja objekts tiek lietots kā bāzes klases tips**.

```cs
class Baze {
    public virtual void Izvade() {
        Console.WriteLine("Bāze");
    }
}

class Atvasinata : Baze {
    public override void Izvade() {
        Console.WriteLine("Atvasināta (override)");
    }
}

class Program {
    static void Main() {
        Baze objekts1 = new Atvasinata(); // tips: Baze
        Atvasinata objekts2 = new Atvasinata(); // tips: Atvasinata

        objekts1.Izvade(); // -> "Atvasināta (override)"
        objekts2.Izvade(); // -> "Atvasināta (override)"
    }
}
```

**Īsumā:**

|                                 | `new` | `override` |
| ------------------------------- | ----- | ---------- |
| Slēpj bāzes metodi              | ✔️    | ❌         |
| Pārraksta bāzes metodi          | ❌    | ✔️         |
| Atbalsta polimorfismu           | ❌    | ✔️         |
| Prasa `virtual`/`abstract` bāzē | ❌    | ✔️         |


#### SOLID
##### Single Responsibility Principle (SRP)
Katras klases vai moduļa atbildība ir ierobežota ar vienu, konkrētu uzdevumu.
##### Open-Closed Principle (OCP)
Princips nosaka, ka klasei jābūt atvērtai paplašināšanai un aizvertai priekš modifikācijām. Tas nozīmē, ka, mainoties prasībām, esošo klasi nevajadzētu modificēt - jaunu funkcionalitāti pievieno, paplašinot risinājumu ar jauniem komponentiem.
##### Liskov Substitution Principle (LSP)
Princips ir nosaukts pēc autores vārda (Barbara Liskov), kura to noformulēja. Princips
nosaka, ka funkcijai, kas apstrādā vecāka klasi (parent class) jāstrādā korekti arī ar
klases bērniem (child classes).
##### Interface Segregation Principle (ISP)
Segregācija ir process, kad izdala kādu elementu no pārējas grupas.
*Pēc būtības līdzīgs dekompozīcijai.*
##### Dependency Inversion Principle (DSP)
Ja burtiski tulkot “Atkārību inversijas princips”, kas noteic, ka funkcijām labāk būt
atkārīgām no abstrakcijām (interfeisiem un abstraktām klasēm) nevis konkrētām
klasēm.
#### Projektēšanas šabloni
##### Builder

**Builder** šablonu izmanto, ja konstruktors satur pārāk daudz parametru un katrs objekts ir unikāls. Šādā gadījumā visu parametru vienlaicīga norādīšana nav ērta, tāpēc tiek izmantots pakāpenisks objekta veidošanas process.

**Prototype** šablona raksturīga iezīme ir tāda, ka objekta īpašības tiek iestatītas, izmantojot metodes, piemēram, `setProperty(param)` vai `AddParameter()`.
##### Builder 2

Lai nebūtu nepieciešams katru parametru iestatīt jaunā rindā, bieži vien **Builder** metodes tiek veidotas tā, lai tās atgrieztu pašu **Builder** objektu, izmantojot `this`. Tādējādi objekta īpašības var iestatīt ķēdes (chain) veidā – vienā izsaukumu virknē.
##### Director of Builder

**Director** tiek izmantots kopā ar **Builder** šablonu. **Director** ir atbildīgs par objektu veidošanas procesa vadību un piedāvā iepriekš definētas īpašību kombinācijas.
##### Prototype

**Prototype** šablons ļauj izveidot vairākus objektus kā kopijas no iepriekš konfigurēta objekta.

Šī šablona galvenā iezīme ir tāda, ka klase spēj sagatavot objektu un pēc tam veidot tā kopijas, izmantojot metodi **`Clone()`**.
##### Singleton

**Singleton** ir neatņemama struktūra situācijās, kad programmēšanas valoda neatbalsta globālus mainīgos. Tas nodrošina, ka visā projektā tiek izveidots tikai viens objekts.

Šī šablona raksturīgā iezīme ir tāda, ka klase nepieļauj vairāku objektu izveidi, bet caur metodi **`getInstance()`** atgriež vienīgo esošo objektu. Konstruktors ir **private**, tāpēc to nevar izsaukt tieši no ārpuses.
##### Abstract Factory

**Abstract Factory** projektēšanas šablonu izmanto, kad nepieciešams radīt objektus vienādā stilā, bet dažādās grupās vai kategorijās.
##### Factory Method

**Factory Method** projektēšanas šablonu izmanto situācijās, kad programma atbalsta moduļus ar vienādiem pamatprincipiem, taču algoritmi un izmantotās klases var atšķirties.
##### Flyweight

**Flyweight** ir struktūras dekompozīcijas šablons, kas ļauj koplietot datus, kuri ir vienādi visiem objektiem, saglabājot tos atsevišķā kopīgā objektā. Tas palīdz samazināt atmiņas (RAM) patēriņu.

**Flyweight** šablona būtība ir tajā, ka mēs izveidojam **koplietojamu objektu,** kurā tiek glabāti **kopīgi dati**, kurus izmanto daudzi citi objekti vai klases.
##### Boxing & Unboxing

**Boxing un Unboxing** nav klasiskā nozīmē projektēšanas šablons, bet gan programmēšanas tehnika, ko izmanto, kad nepieciešams nodot metodei dažādus datu tipus **bez metodes pārlādēšanas (overload)**.

**Boxing** nozīmē, ka **vērtību tipa** dati (piemēram, `int`, `bool`) tiek ietverti kā **objekti** (reference type), lai tos varētu apstrādāt kā vienotu tipu.  
**Unboxing** ir pretējais process — objekts tiek pārvērsts atpakaļ par konkrētu vērtību tipu.
##### Facade

**Facade** (strukturālais šablons) ir projektēšanas šablons, kas ļauj **paslēpt sarežģītu sistēmas uzbūvi**, piedāvājot vienkāršu un vienotu saskarni darbam ar vairākām iekšējām komponentēm.
##### Proxy

**Proxy** (strukturālais šablons) tiek izmantots, lai **kontrolētu piekļuvi pie citu klašu funkcionalitātes**, piemēram, resursietilpīgām metodēm vai ārējiem servisiem.
##### Adapter

**Adapter** (strukturālais šablons) tiek izmantots, kad nepieciešams **izveidot savienojumu starp divām nesaistītām sistēmām vai komponentēm**, kuras **nav iespējams tieši modificēt**.
##### Iterator

**Iterator** ir projektēšanas šablons, kas ļauj **pakāpeniski pārstaigāt kolekciju (piemēram, sarakstu, koku, u.c.) bez nepieciešamības tieši izmantot indeksus**.
##### Chain of Responsibility

**Chain of Responsibility** (atbildības ķēde) ir projektēšanas šablons, kas nodrošina **datu vai pieprasījuma apstrādi secīgu posmu veidā**. Katrs posms pats izlemj, vai apstrādāt pieprasījumu, vai nodot to tālāk nākamajam posmam ķēdē.
##### State

**State** ir projektēšanas šablons, kas balstās uz **galīgiem stāvokļu automātiem (Finite-State Machine)** un tiek izmantots, lai aprakstītu objektu uzvedību atkarībā no to **iekšējā stāvokļa**.
##### Visitor

**Visitor** ir projektēšanas šablons, kas ļauj **definēt operācijas dažādiem objektu tipiem**, neieviešot šīs operācijas pašās datu klasēs. To izmanto, kad **polimorfisms nav iespējams** (piemēram, kad objekti nepieder vienai mantošanas hierarhijai vai mantošana ir aizliegta).

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Navigācija - OOP vispārīgi]]

---