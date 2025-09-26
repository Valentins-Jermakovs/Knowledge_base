**Datums:** 2025-04-27   
**Laiks:** 21:19 

❚ **Tagi:**  #OOP 
⌬ **Objekts:**  `OOP`

---
### ⬢ Detalizēts apraksts
#### Tēma 1 - Ievads
Šajā rakstā tiek apskatīti trīs galvenie objektorientētas programmēšanas (OOP) jēdzieni: **asociācija**, **salikums** un **apvienojums**, kas tiek izmantoti klasēs, lai attēlotu dažādas attiecības starp objektiem.

> [!NOTE] Asociācija
> **Asociācija** norāda uz saikni starp diviem objektiem, kas var pastāvēt neatkarīgi, bet ir savstarpēji saistīti, piemēram, autors un grāmata.
  
> [!NOTE] Salikums
> **Salikums** (composition) apraksta ciešu saikni, kur viens objekts ir daļa no cita un nevar pastāvēt patstāvīgi, piemēram, grāmata un tās lappuses. Ja objekts tiek iznīcināts, tā daļas tiek iznīcinātas līdz ar to.

> [!NOTE] Apvienojums
> **Apvienojums** (aggregation) attēlo vājāku saikni, kur objekts pārvalda citus, bet tie var pastāvēt neatkarīgi. Piemērs ir bibliotēka un tās grāmatas, kur grāmatas var pastāvēt arī ārpus bibliotēkas.
#### Tēma 2 - Asociācija

Asociācija ir saikne starp divām klasēm, kas nozīmē, ka to objekti var mijiedarboties vai būt saistīti. Atšķirībā no citām attiecībām, asociācija neparedz stingru atkarību, un objekti var eksistēt neatkarīgi cits no cita. Šī saikne var būt gan vienvirziena, gan abpusēja, atkarībā no tā, kā tiek definēta saikne starp klasēm.

<mark style="background: #ADCCFFA6;">Objekti, kas saistīti ar asociāciju, var pastāvēt viens bez otra. Tie nav stingri atkarīgi viens no otra.</mark>

>Asociācijai var būt dažādas formas atkarībā no attiecību veida starp objektiem:
>- **Vienkārša**: Piemēram, autors un grāmata, kur katram autoram ir viena grāmata;
>- **Daudz uz vienu**: Viens autors var sarakstīt vairākas grāmatas;
>- **Viens uz vienu**: Katram autoram ir tieši viena grāmata.

**Koda piemērs:**

```cs
class Author //klases nosaukums
{
	//lauki (atribūti)
    private Book book;
    //metodes
    public void SetBook(Book book) 
    {
	    this.book = book;
	}
}

class Book //klases nosaukums
{
	//lauki (atribūti)
    private Author author;
    //metodes
    public void SetAuthor(Author author) 
    {
		this.author = author;
	}
}
```

Klase **Author** un klase **Book** ir saistītas ar asociāciju, kur katra klase satur atsauces uz otru. Tātad, **Author** satur atsauci uz **Book**, un **Book** satur atsauci uz **Author**.

Objekti tiek izveidoti atsevišķi, un saite starp tiem tiek noteikta, izmantojot metodes, piemēram, `SetBook` un `SetAuthor`. Tātad katrs objekts ir neatkarīgs, bet tie var mijiedarboties, izmantojot metodes, kas ļauj noteikt to attiecības.

>Lai pilnībā izprast asociācijas, mums nepieciešams apskatīt šo realizāciju pilnībā.

Klase `Author`:

```cs
class Author //klases nosaukums
{
	//atribūti
	private String name;
	private String surname;
	private Book book; //šis atribūts veido citas klases objektu
	//metodes
	public Author(String name, String surname) //konstruktors
	{
		this.name = name;
		this.surname = surname;
	}
	public String Name //private tipa datu nolasīšana
	{ 
		get { return name; }
	}
	public String Surname //private tipa datu nolasīšana
	{ 
		get { return surname; }
	}
	public Book Book //citas klases objekta pievienošana
	{
		set { book = value; }
	}
	public void Info() //informācijas izvade
	{
		//metodes loģika
		if (book != null)
		{
			Console.WriteLine("{0} {1} is author of {2}.", name, surname, book.Title);
		}
		else
		{
			Console.WriteLine("{0} {1} is author.", name, surname);
		}
	}
}
```

Un tagad tiek apskatīta klase `Book`, ko izmanto klase `Author`:

```cs
class Book //klases nosaukums
{
	//atribūti
	private String title;
	private Author author; //izveido klases Author objektu
	//metodes
	public Book(String title) //konstruktors
	{
		this.title = title;
	}
	public String Title //private tipa datu nolasīšana
	{
		get { return title; }
	}
	public Author Author //sasaista Book ar Author
	{
		set { author = value; }
	}
	public void Info() //izvada informāciju
	{
		//metodes loģika
		if (author != null)
		{
			Console.WriteLine("{0} is written by {1} {2}.", title, author.Name, author.Surname);
		}
		else
		{
			Console.WriteLine("{0} is book.", title);
		}
	}
}
```

Vienkārši sakot, šis klases izmanto viena otru savās metodes, ir saistītas savā starpā, taču `Book` var eksistēt bez `Author`, kā arī pats `Autohor` var eksistēt bez `Book`, lai gan kodā tam ir metodes, lai veikts savstarpējo saisti.

Un tagad tieši, kā tiek veidoti šādi objekti un kā tos saistīt savā starpā:

```cs
class Program //programma
{
	static void Main(string[] args) //Main bloks
	{
		//šeit tiek izveidots objekts tipa Autors
		Author author = new Author("Jules", "Vern");
		//šeit tiek izveidots objekts tipa grāmatata (book)
		Book book = new Book("80 days around the world");
		//izvada informāciju pirms objekti esot saistīti
		Console.WriteLine("---Before---");
		author.Info();
		book.Info();
		//šajā daļā objekti jau tiek savā starpā savienoti
		Console.WriteLine("\n\n---After---");
		author.Book = book;   //pie autora pievieno grāmatu
		book.Author = author; //autoru pievieno pie grāmatas
		//informācijas izvads mainīsies, jo objekti tagad esot saistīti
		author.Info();
		book.Info();
		Console.ReadKey();
	}
}
```

Analizējot piemēru, mēs varam saprast, kā **Asociācija** ļauj mums izveidot <mark style="background: #FFB86CA6;">2 objektus</mark>, kas var būt <mark style="background: #FFB86CA6;">neatkarīgi</mark>, nesaistīti viens ar otru, <mark style="background: #FFB86CA6;">taču</mark> to kodā realizēts <mark style="background: #FFB86CA6;">funkcionāls</mark>, kas <mark style="background: #FFB86CA6;">ļauj sasaistīt šos 2 objektus savā starpā</mark>, bet nav obligāts.
#### Tēma 3 - Salikums

Salikums (composition) ir <mark style="background: #ADCCFFA6;">stipra saikne starp klasēm, kurā viens objekts (veselums) sastāv no citiem objektiem (daļām)</mark>. Šajās attiecībās <mark style="background: #ADCCFFA6;">daļas nevar pastāvēt neatkarīgi no veseluma.</mark> Ja veselums tiek iznīcināts, tiek iznīcinātas arī visas tā daļas, jo tās ir cieši saistītas ar veselumu un nevar pastāvēt bez tā.

Daļas (komponenti) ir tieši atkarīgas no veseluma, un tās nevar pastāvēt patstāvīgi ārpus tā. Daļu izveide un iznīcināšana tiek kontrolēta ar veselumu, kas nozīmē, ka visas daļas tiek iznīcinātas, kad tiek iznīcināts veselums.

>Kā teorētiskus piemērus, mēs varam paņemt:
>- **Grāmata un tās lappuses**: Lappuses nevar pastāvēt bez grāmatas, jo tās ir tās daļa;
>- **Auto un tā dzinējs**: Dzinējs nepieder citam auto, tas ir neatņemama daļa no konkrēta auto.

**Koda piemērs:** Klase **Book** satur masīvu ar **Page** objektiem. Šajā gadījumā **Book** ir veselums, bet **Page** ir tā daļas. Lappuses tiek izveidotas un pārvaldītas tieši grāmatas ietvaros, un tās nevar eksistēt ārpus grāmatas.

```cs
class Book {
    private Page[] pages;  // Kompozīcija: lappuses pieder grāmatai
    //metode
    public Book(string title) 
    {
        pages = new Page[10];  // Lappuses tiek izveidotas grāmatas konstruktorā
        for (int i = 0; i < 10; i++) {
            pages[i] = new Page(i, "Text...");
        }
    }
}

class Page {
    private int number;
    private string text;
    public Page(int num, string t) 
    {
        number = num;
        text = t;
    }
}
```

Kā redzams piemērā, objekti tipa `Page` netiek veidoti atsevišķi, kā iepriekšējā tēmā. Izveidojot grāmatu, mēs vienlaikus izveidojam arī tās lappuses, jeb 10 objektus tipa `Page` un ierakstam tās masīvā `pages`.

<mark style="background: #FFB86CA6;">Tādējādi, izdzēšot grāmatu, tiek izdzēsts arī tas masīvs ar Page objektiem.</mark>

>Lai pilnībā saprast šo saikni, izpētīsim katru klasi atsevišķi.

Klase `Book`:

```cs
class Book //klases nosaukums
{
	//atribūti
	private String title;
	private Author author;
	private Page[] pages;  //masīvs ar objektiem Page
	private int pageNumber;
	//metodes
	public Book(String title) //konstruktors
	{
		this.title = title;
		Console.WriteLine("Number of pages: ");
		pageNumber = int.Parse(Console.ReadLine()); //sagaida ievadu
		//pārbaude uz lpp skaitu
		if(pageNumber < 1)
		{
			pageNumber = 1;
		}
		
		pages = new Page[pageNumber]; //izveido masīvu ar objektiem Page
		
		String t = "t";
		for(int i=0; i < pageNumber; i++) //aizpilda ar t burtiem atbilstoši lapas numuram
		{
			pages[i] = new Page(i, t);
			t += t;
		}
	}
	public String ReadPage(int number) //nolasa lappuses saturu
	{
		if (number > -1 && number < pageNumber)
		{
			return pages[number].Text;
		}
		else
		{
			return "Page not found";
		}
	}
	public void Info() //izvada informāciju par grāmatu
	{
		if (author != null)
		{
			Console.WriteLine("{0} is written by {1} {2}.", title, author.Name, author.Surname);
		}
		else
		{
			Console.WriteLine("{0} is book.", title);
		}
		Console.WriteLine("It contains {0} pages.", pageNumber);
	}
}
```

Šeit galvenais saprast, kā veidojot grāmatu, mēs tajā ierakstam lappušu skaitu, un veidojom šos te `Page` tipa objektu atbilstoši lietotāja ievadam un ierakstam šos objektus masīvā `pages`, kā arī aizpildām to saturu ar `t` burtiem.

Un šeit apskatīsim jau šo pakļauto klasi, kas nevar eksistēt pati pa sevi:

```cs
class Page //klases nosaukums
{
	//atribūti
	private int number;
	private String text;
	//metodes
	public Page(int number, String text) //konstruktors
	{
		this.number = number;
		this.text = text;
	}
	public int Number //nolasa private tipa datus
	{ 
		get { return number; }
	}
	public String Text //nolasa private tipa datus
	{ 
		get { return text; }
	}
}
```

Kā redzam, tehnsiki, šeit nekādu saistību ar klasi `Book` nav, taču šī te klase tiek izmantota objekta tipa `Book` izveides laikā. <mark style="background: #FFB86CA6;">Page šajā gadījumā ir vienums, kas pakļauts veselumam.</mark>

Nu un proti, piemērs, kā tiek veidots šāda tipa objekts:

```cs
static void Main(string[] args) //Main() bloks
{
	Book book = new Book("80 days around the world"); //tiek veidots objekts tipa Book
	//tātad, papildus tam tiek izveidotas vēl lappuses
	book.Info(); //izvada info par grāmatu
	Console.Write("Page of book: ");
	int toRead = int.Parse(Console.ReadLine()); //saglabā lietotāja ievadu
	Console.WriteLine(book.ReadPage(toRead)); //nodod ievadu funkcijai
	Console.ReadKey();
}
```

Šādi izskatās **Salikums**, tātad, <mark style="background: #ADCCFFA6;">eksistē viens liels objekts, kuram pakļauts cits objekts.</mark>
#### Tēma 4 - Apvienojums

Apvienošana (aggregation) ir vājāka saikne starp klasēm, kurā viens <mark style="background: #ADCCFFA6;">objekts (konteineris) satur vai pārvalda citus objektus (komponentus)</mark>, bet šie komponenti var pastāvēt neatkarīgi no konteinera. <mark style="background: #ADCCFFA6;">Ja konteiners tiek iznīcināts, komponenti var turpināt eksistēt patstāvīgi.</mark>

Komponenti nav tieši atkarīgi no konteinera. Tie var pastāvēt patstāvīgi un tikt izmantoti arī citos konteinieros. Komponentus var pārvietot starp dažādiem konteineriem vai izmantot arī ārpus tiem.

>Kā teorētiskos piemērus, varam paņemt:
>- **Bibliotēka un grāmatas**: Grāmatas var pastāvēt arī ārpus bibliotēkas, jo tās nav tieši atkarīgas no tās eksistences, kā arī bibliotēkas var apmainīties ar grāmatām;
>- **Auto un tā riepas**: Riepas var pārmest citam auto, jo tie nav neatņemama sastāvdaļa no konkrētā auto. Riepas esot universālas un der katram auto.

**Koda piemērs:** Klase **Library** satur sarakstu ar **Book** objektiem. Šajā gadījumā **Library** ir konteiners, bet **Book** ir komponents. Grāmatas var tikt pievienotas un noņemtas no bibliotēkas, un tās var turpināt eksistēt patstāvīgi, pat ja tās tiek izņemtas no bibliotēkas.

```cs 
class Library //klases nosaukums
{
	//atribūti
    private List<Book> books;  // Apvienošana: grāmatas var būt ārpus bibliotēkas
    //metodes
    public void AddBook(Book book) //pievieno grāmatu pie bibliotēkas
    {
        books.Add(book); //pievieno objektu pie masīva
    }
    public Book RemoveBook(int id) //dzēš grāmatu no bibliotēkas
    {
        Book book = books[id]; //iegūst grāmatas id
        books.RemoveAt(id); //izdēš grāmatu no bibliotēkas
        return book;  // Grāmata tiek atgriezta un turpina eksistēt ārpus bibliotekas
    }
}
```

Komponenti (**Book**) tiek izveidoti ārpus konteinera (**Library**). Konteiners pārvalda komponentu kolekciju, bet neiznīcina tos, kad pats tiek iznīcināts. Komponenti var turpināt pastāvēt un tikt izmantoti citos konteinieros. <mark style="background: #FFB86CA6;">Vienkārši sakot, bibliotēka atsaucas uz objektiem tipa Book.</mark>

Pilnīgs klases `Library` apskats:

```cs
class Library //klases nosaukums
{
	//atribūti
	private String address;
	private List<Book> books = new List<Book>(); //tiek veidots tukšs grāmatu masīvs
	//metodes
	public Library(String address) //konstruktors
	{
		this.address = address;
	}
	public void AddBook(Book book) //grāmatas pievienošana
	{
		books.Add(book);
	}
	public Book RemoveBook(int id) //grāmatas dzēšana
	{
		Book b = books[id];
		if(id > -1 && id < books.Count)
		{
			books.RemoveAt(id);
		}
		return b;
	}
	public void PrintList() //grāmatu daudzuma izvade
	{
		if (books.Count > 0)
		{
			for (int i = 0; i < books.Count; i++)
			{
				books[i].Info();
			}
		}
		else
		{
			Console.WriteLine("Library doesn't contain some book!");
		}
	}
}
```

Un tagad kā izskatās šādas bibliotēkas izveide:

```cs
static void Main(string[] args) //Main() bloks
{
	//tiek izveidotas grāmatas
	Console.WriteLine("---Create books---");
	Book book1 = new Book("80 days around the world");
	Book book2 = new Book("Alice in Wonderland");
	//tiek veidota bibliotēka
	Console.WriteLine("---Create library---");
	Library library = new Library("Str. Atbrivošanas 115");
	library.PrintList();
	//pie bibliotēkas pievieno grāmatas, veido atsauci
	Console.WriteLine("---Add books---");
	library.AddBook(book1);
	library.AddBook(book2);
	library.PrintList();
	//grāmatas tiek izdzēstas un saglabātas ārpus
	Console.WriteLine("---Remove book---");
	Book book3 = library.RemoveBook(0);
	//izvada bibliotēkas saturu
	library.PrintList();
	Console.ReadKey();
}
```

Ja bibliotēka (**Library**) iznīcina sevi (t.i., <mark style="background: #ADCCFFA6;">ja tiek izdzēsta pati Library klase), grāmatas Book nebūs iznīcinātas, jo tās ir tikai referencētas (atsauces) bibliotēkā</mark>, nevis daļa no tās dzīves cikla. Tās var turpināt pastāvēt patstāvīgi.

---
### ⚛ Secinājums/i

<mark style="background: #FFB86CA6;">Asociācija: kad objekti pastāv neatkarīgi viens no otra, bet var tikt saistīti;</mark>
<mark style="background: #FFF3A3A6;">Salikums: kad viens objekts izmanto citu objektu, atsevišķi tie nespējs eksistēt;</mark>
<mark style="background: #BBFABBA6;">Apvienojums: kad viens objekts atsaucas uz citu objektu. Ir viens veselums ar atsauci uz vairākiem vienumiem.</mark>

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Klases, kas tas ir]]
Nākama lapa >>> [[Mantošana un polimorfisms]]

---