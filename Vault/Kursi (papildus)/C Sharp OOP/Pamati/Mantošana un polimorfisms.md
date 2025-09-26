**Datums:** 2025-04-27   
**Laiks:** 21:44 
❚ **Tagi:**  #OOP 

⌬ **Objekts:**  `OOP`

---
### ⬢ Detalizēts apraksts
#### Tēma 1 - Ievads
Mantošana ļauj apakšklasei iemantot virsklases īpašības un metodes, tādējādi nodrošinot koda pārstrādājamību un struktūru. C# ļauj izmantot vienkāršu un daudzlīmeņu mantošanu.

> [!NOTE] Mantošana
> Mehānisms, kas ļauj vienai klasei pārmantot citas klases funkcionalitāti.

> [!NOTE] Virsklase (superclass) 
> Bāzes klase, no kuras manto funkcionalitāti.

> [!NOTE] Apakšklase (subclass)
> Klase, kas manto virsklases īpašības un metodes, un var tās papildināt vai pārrakstīt.

> [!NOTE] base()
> Atsauce uz virsklases konstruktoru.

> [!NOTE] new
> Ļauj izmantot virsklases metodi.
#### Tēma 2 - Klases mantošana

Mantošana ir saite, kad viena klase iemanto visas metodes un
laukus no vecākklases/virsklases (parent class, superclass).

>Piemēram, mums ir 3 klases, kas manto metodes no virsklases, konkrēti:
>- Building;
>- Hotel;
>- Fabric.

Klases `Building` koda piemērs:

```cs
class Building //klases nosaukums
{
	//atribūti
	private string address;
	private string builtDate;
	//metodes
	public Building() //konstruktors
	{
		Console.Write("Address: ");
		address = Console.ReadLine();
		Console.Write("Date: ");
		builtDate = Console.ReadLine();
	}
	public string Address //nolasa adresi
	{ 
		get { return address; } 
	}
	public string Date //nolasa datumu
	{ 
		get { return builtDate; } 
	}
	public void WriteInfo() //info izvade
	{
		Console.WriteLine("Building {0} is constructed in {1}", address, builtDate);
	}
}
```

Kā redzams piemērā, virsklasē `Building` nekā īpaša nav, tāpēc kā tā ir klase, kuras metodes un atribūtus mantos citas klases.

Un tagad tiks apskatīta klase `Hotel`, kas jau manto dažas lietas no virsklases `Building`:

```cs
class Hotel: Building // : Building norāda kā klase Hotel manto Building
{
	private string name;
	private int roomsNumber;
	//metodes
	public Hotel(): base() //konstruktors  manto datus no Building
	{
		Console.Write("Name of hotel: ");
		name = Console.ReadLine();
		Console.Write("Number of rooms: ");
		roomsNumber = int.Parse(Console.ReadLine());
	}
	public new void WriteInfo() //vārds new ļauj pielietot metodi no virsklases
	{
		base.WriteInfo(); //metode no virsklases
		Console.WriteLine("It is hotel {0} with {1} rooms", name, roomsNumber);
	}
}
```

Tagad, analizējot šo piemēru, var saprast, kā lai apakšklase mantotu virsklasi, nepieciešama šāda sintakse `apakšklases_nos : virsklases_nos`.
Un, lai apakšklases konstruktors spētu darboties ar virsklases atribūtiem, pielieto šādu sintaksi `konstruktora_nos(): base()`.

Bet, lai jau izmantot apakšklasēs metodē virsklases metodes, izmanto atslēgvārdu `new` Tas ļaus piekļūt pie virsklases metodēm, piem., `base.WriteInfo()`.
*Sanāk kā apakšklase, kad izpilda tās metodes, var izsaukt virsklases metodes.*

Un vēl viens piemērs, tagad klase `Fabric`, tās virsklase arī ir `Building`:

```cs
class Fabric: Building //manto virsklasi Building
{
	//atribūti
	private string name;
	private int workerNumber;
	private string production;
	//metodes
	public Fabric(): base() //konstruktors manto virsklases datus
	{
		Console.Write("Name of fabric: ");
		name = Console.ReadLine();
		Console.Write("Number of workers: ");
		workerNumber = int.Parse(Console.ReadLine());
		Console.Write("Produce: ");
		production = Console.ReadLine();
	}
	public new void WriteInfo() //vārds new ļauj mantot metodes
	{
		base.WriteInfo(); //izsauc virsklases metodi
		Console.WriteLine("It is factory {0} with {1} rooms.", name, workerNumber);
		Console.WriteLine("Which produces {0}.", production);
	}
}
```

Atšķirība ir tieši objektu izveidē:

```cs
static void Main(string[] args) //Main() bloks
{
	//tiek izveidots objetks Hotel
	Console.WriteLine("---Hotel---");
	Hotel hotel = new Hotel();
	hotel.WriteInfo();
	Console.ReadKey();
}
```

**BET!!!** tā kā klase Hotel manto virsklasi `Building`, programmas izvads būs šāds:

![[Pasted image 20250427214939.png]]

Sākumā izsaucas virsklases konstruktors, kur lietotājs ievada laukus `Address` un `Date`. Sanāk, kā sākumā tiek aizpildīts `Building` konstruktors un tikai pēc tam, lietotājs aizpilda klases `Hotel` konstruktora laukus, šeit tie ir `Name of hotel` un `Number of rooms`.
Pēc tam klase `Hotel` izsauc savu metodi `public new void WriteInfo()`, kurā sākumā tiek izsaukta virsklases metode `WriteInfo()` un jau pēc tās tiek izpildīts pārējais kods.

*Identiski ir objekta tipa `Factory` izveidošanu.* Sākumā tiks aizpildīti lauki virsklases `Building` konstruktorā un pēc tam jau apakšklases lauki. Ar funkcijām arī tas pats.
#### Tēma 3 - Polimorfisms

> Polimorfisms ir īpašība, kad objekts var pieņemt virsklašu datutipus un var strādāt, izmantojot virsklašu loģiku.

Vienkāršiem un saprotamiem vārdiem, <mark style="background: #ADCCFFA6;">mēs konvertējam objektu no vienas klases citā, mainām datu tipu</mark>, līdzīgi kā string pārvērst uz double.

```cs
static void Main(string[] args)
{
	//tiek izveidots objekts hotel datu tipa Hotel
	Console.WriteLine("---Hotel---");
	Hotel hotel = new Hotel();
	hotel.WriteInfo();
	//objekts hotel tiek konvertēts uz datu tipu Building
	Building building = (Building)hotel;
	Console.WriteLine("\n\n---After convertion---");
	building.WriteInfo();
	Console.ReadKey();
}
```

Zemāk tiek attēlots programmas izvads:

![[Pasted image 20250427215149.png]]

Kā redzam, sākumā tiek veidots objekts, kas pieder klasei `Hotel`, un tāpēc tiek aizpildīti virsklase konstruktora lauki, pēc tam jau pašas klases `Hotel` konstruktors un funkcija. Sākumā izsauc virsklases funkciju un pēc tam izpilda jau `Hotel` klase kodu.

Taču pēc konvertācijas, kā redzams, dati objektam `hotel`, kas bija attiecināmi uz klasi `Hotel`, vairs nav pieejami un paliekt tikai tie, kas pieder virsklasei. Bet, ja pēc tam konvertēt objektu atpakaļ uz apakšklasi, kurai tas bija piederējis sākumā, piekļuve pie datiem tiks atjaunota.

<mark style="background: #FFB86CA6;">Pēc konvertācijas dati nepazūd! Virsklasei vienkārši nav pieejas pie apakšklases datiem (laukiem).</mark>

---
### ⚛ Secinājums/i

>Mantošana palīdz veidot strukturētu kodu, kas balstās uz hierarhijām. Tā ļauj efektīvi izmantot esošo funkcionalitāti un paplašināt to jaunās klasēs.

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Saites starp klasēm]]
Nākama lapa >>> [[Interfeiss un nosaukumvieta]]

---