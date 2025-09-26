⏲ **Datums:** 2025-04-28   
⏲ **Laiks:** 16:23 
❚ **Tagi:**  #OOP

⌬ **Objekts:**  `OOP`

---
### ⬢ Detalizēts apraksts
#### Tēma 1 - Ievads

Šajā rakstā tiek aplūkotas trīs galvenās objektorientētās programmēšanas attiecību koncepcijas Python valodā: **Asociācija**, **Salikums** un **Apvienojums**. Katra no šīm attiecībām ļauj mums modelēt dažādas saistības starp objektiem, nodrošinot elastīgu un modulāru programmatūras arhitektūru. Rakstā sniegts teorētisks skaidrojums katram jēdzienam, kā arī praktiski Python koda piemēri, kas ilustrē, kā šīs attiecības tiek realizētas praksē.

> [!NOTE] Asociācija
> Attēlo saikni starp diviem objektiem, kuri var eksistēt neatkarīgi, bet var savstarpēji mijiedarboties.

> [!NOTE] Salikums
> Apraksta attiecību, kur viens objekts sastāv no citiem objektiem, kas nevar pastāvēt patstāvīgi (daļas ir neatņemama veseluma sastāvdaļa).

> [!NOTE] Apvienojums
> Norāda uz situāciju, kad objekts satur citus objektus, taču šie komponenti var eksistēt neatkarīgi no konteinera.
#### Tēma 2 - Asociācija

Asociācija ir attiecības, kurās divi objekti ir savstarpēji saistīti, tomēr tie pastāv neatkarīgi. Piemēram, klase `Author` var saturēt atsauci uz `Book`, bet abu objektu dzīves cikli nav savstarpēji sasaistīti.

```python
class Author:
    def __init__(self, name):
        self.name = name
        self.book = None  # Sākotnēji nav saistīts ar grāmatu

    def set_book(self, book):
        self.book = book

    def info(self):
        if self.book:
            print(f"{self.name} is the author of '{self.book.title}'.")
        else:
            print(f"{self.name} is an author.")

class Book:
    def __init__(self, title):
        self.title = title
        self.author = None  # Sākotnēji nav saistīts ar autoru

    def set_author(self, author):
        self.author = author

    def info(self):
        if self.author:
            print(f"'{self.title}' is written by {self.author.name}.")
        else:
            print(f"'{self.title}' is a book.")

# Objektu izveide
author = Author("Jules Vern")
book = Book("80 Days Around the World")

# Pirms sasaistes
print("--- Before association ---")
author.info()
book.info()

# Sasaistam objektus
author.set_book(book)
book.set_author(author)

print("\n--- After association ---")
author.info()
book.info()
```

Šeit katrs objekts tiek izveidots neatkarīgi, un sasaistīšana notiek, izmantojot metodes `set_book` un `set_author`.
#### Tēma 3 - Salikums

Salikums nozīmē stipru saikni, kur vienam objektam (veselumam) ir neatņemama sastāvdaļa. Ja veselums tiek iznīcināts, arī visas tā daļas tiek iznīcinātas. Piemēram, grāmatai ir lappuses, un, ja grāmata pazūd, arī tās lappušu vairs nav.

```python
# Klase Pgae
class Page:
    def __init__(self, number, content):
        self.number = number      # Lapas numurs
        self.content = content    # Lapas saturs

# Klase Book
class Book:
    def __init__(self, title, page_count):
        self.title = title
        self.pages = []  # Tukšais masīvs lapu glabāšanai

        # Izveido vajadzīgo lappušu daudzumu
        for i in range(page_count):
            page_number = i + 1  # Lapu numerāciju sākas ar 1
            content = f"Content of page {page_number}"
            page = Page(page_number, content)
            self.pages.append(page)  # Pievieno lapu grāmatā

    # Metode lapas satura lasīšanai
    def read_page(self, page_number):
        if 1 <= page_number <= len(self.pages):
            page = self.pages[page_number - 1]
            return f"Page {page.number}: {page.content}"
        else:
            return "Page not found."

    # Metode informācijas izvadei par grāmatu
    def info(self):
        print(f"'{self.title}' has {len(self.pages)} pages.")

# Izveido grāmatas objektu ar 5 lpp
book = Book("Python Programming", 5)
book.info()
print(book.read_page(3))
```

Šeit klase `Book` izveido savas daļas – objektus `Page` – konstruktorā. Ja grāmata tiek izdzēsta, arī lappuses (daļas) tiek izdzēstas, jo tās nav veidotas ārpus tās struktūras.
#### Tēma 4 - Apvienojums

Apvienojums raksturo vājāku saikni, kurā objekts (konteineris) satur citus objektus, bet tie var eksistēt patstāvīgi. Piemēram, bibliotēka satur grāmatas, taču grāmatas var pastāvēt arī ārpus bibliotēkas.

```python
class Book:
    def __init__(self, title):
        self.title = title

    def info(self):
        print(f"Book: '{self.title}'")

class Library:
    def __init__(self, address):
        self.address = address
        self.books = []  # Saraksts ar grāmatām

    def add_book(self, book):
        self.books.append(book)

    def remove_book(self, index):
        if 0 <= index < len(self.books):
            return self.books.pop(index)
        else:
            print("Invalid index.")
            return None

    def print_library(self):
        print(f"Library at {self.address} contains:")
        if self.books:
            for book in self.books:
                book.info()
        else:
            print("No books available.")

# Objektu izveide
book1 = Book("80 Days Around the World")
book2 = Book("Alice in Wonderland")

library = Library("Str. Atbrivošanas 115")
library.print_library()

print("\n--- Adding books ---")
library.add_book(book1)
library.add_book(book2)
library.print_library()

print("\n--- Removing a book ---")
removed_book = library.remove_book(0)
library.print_library()
print("Removed book:")
removed_book.info()
```

Šeit klase `Library` pārvalda grāmatu sarakstu, bet grāmatas (klase `Book`) tiek izveidotas ārpus bibliotēkas. Ja bibliotēka tiek izdzēsta, grāmatas var pastāvēt turpmāk, jo tās ir saistītas ar bibliotēku tikai kā atsauces.

---
### ⚛ Secinājums/i

>Python ļauj modelēt dažādas saistības starp objektiem, izmantojot:
>- **Asociāciju** – objekti var pastāvēt neatkarīgi, bet tiem var būt savstarpēja saikne.
>- **Salikumu (composition)** – objekti ir cieši saistīti; veselums satur daļas, kuras nepastāv neatkarīgi.
>- **Apvienojumu (aggregation)** – konteineris pārvalda citus objektus, tomēr tie var eksistēt arī ārpus tā struktūras.

Izmantojot šīs attiecību formas, mēs varam veidot skaidru un modulāru kodu, kas atvieglo programmas uzturēšanu un atkārtotu izmantošanu.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Inkapsulācija, atribūti un īpašības]]
Nākama lapa >>> [[Abstraktās klases Python]]

---