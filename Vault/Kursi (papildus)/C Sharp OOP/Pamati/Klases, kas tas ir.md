**Datums:** 2025-04-27   
**Laiks:** 21:09 

❚ **Tagi:**  #OOP
⌬ **Objekts:**  `OOP`

---
### ⬢ Detalizēts apraksts
#### Tēma 1 - Ievads

Darbojoties ar objektorientēto programmēšanu, ir svarīgi saprast pamatjēdzienus, piemēram, klases, objektus, atribūtus un konstruktorus. Šie jēdzieni veido pamatu jebkurai C# programmai, kas balstīta uz datu un funkcionalitātes strukturētu organizēšanu. Šajā rakstā ir apkopota būtiskākā informācija, lai viegli un saprotami apgūtu, kā veidot klases un izmantot tās praktiskos piemēros.

> [!NOTE] Klase
> **Klase**: loģiska datu un funkciju grupa, kas attēlo kādu vienību vai priekšmetu (šablons).

> [!NOTE] Objekts
> **Objekts**: konkrēts klases piemērs (eksemplārs).

> [!NOTE] Lauki/atribūti
> **Lauki / atribūti**: mainīgie, kas pieder klasei.

> [!NOTE] Konstruktors
> **Konstruktors**: īpaša funkcija, kas tiek izmantota objekta izveidei.
#### Tēma 2 - Klases struktūra

```cs
class Animal //tas ir klases nosaukums
{
	//šie te ir lauki jeb klases atribūti
	public string name;    //atribūts name
	public double weight;  //atribūts weight
	public int age;        //atribūts age

	//šis te ir konstruktors
	public Animal (string n, double w, int a)
	{
		this.name = n;
		this.weight = w;
		this.age = a;
	}
}
```
#### Tēma 3 - Objekta izveide

```cs
static void Main() //programmas galvenais bloks
{
	//objekta izveidošana un parametru nodošana konstruktoram
	Animal an = new Animal("Zaķis", 25.6, 5);
	//objekta atribūtu nolasīšana - info izvade
	Console.Write(an.name + ":" + an.weight + "kg" + an.age + "years.");
	Console.ReadKey();
}
```

Tātad, lai izveidot objektu, vispirms, jāizveido pati klase.
Pēc klases izveides, jāpariet `Main()` blokā.

<mark style="background: #FFB86CA6;">Objekta izveidei tiek izmantota šāda sintakse:</mark>

```cs
static void Main() //programmas galvenais bloks
{
	Klases_nosaukums objekta_nos = new Objekta_konstruktors();
}
```

Tādējādi tiek izveidots jauns objekts, konstruktoram, atkarībā no tā, vai tam ir aprakstīti parametri, var tos nodod vai nenodod, atkarībā no jūsu koda.

<mark style="background: #ADCCFFA6;">P.S Klasēm atribūtos (tas mainīgajiem) var piešķirt arī noklusējuma vērtības.</mark>

---
### ⚛ Secinājums/i

>**Klase ir pamatelements objektorientētā programmēšanā**, kas kalpo kā šablons datu un funkcionalitātes organizēšanai vienā vienībā.
>**Objekti tiek veidoti no klasēm**, un katrs objekts ir konkrēts klases piemērs ar savām vērtībām.
>**Lauki jeb atribūti glabā objekta stāvokli**, savukārt **konstruktors ļauj šo stāvokli uzreiz inicializēt**, veidojot objektu.

<mark style="background: #ADCCFFA6;">Lai izveidotu objektu, ir nepieciešams:</mark>

- Izveidot klasi ar atribūtiem un konstruktoru;
- `Main()` blokā izmantot konstruktoru objekta izveidei;
- Izmantojot punktu notāciju (`objekts.atribūts`), piekļūt objekta datiem.

**C# programmēšanā ir iespējams arī iestatīt noklusējuma vērtības klases atribūtiem**, kas vienkāršo objektu veidošanu, ja ne visi parametri ir nepieciešami.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - C Sharp OOP]]
Nākama lapa >>> [[Saites starp klasēm]]

---