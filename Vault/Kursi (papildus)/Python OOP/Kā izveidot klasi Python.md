⏲ **Datums:** 2025-04-28   
⏲ **Laiks:** 08:41 
❚ **Tagi:**  #OOP

⌬ **Objekts:**  `OOP`

---
### ⬢ Detalizēts apraksts
#### Tēma 1 - Ievads
Šajā materiālā tiek izskaidrots, kā Python ļauj izveidot savas klases ar atslēgas vārdu `class`, kā darbojas konstruktoru (**__init__()**), kā tiek definēti objekta atribūti, kā arī, kā strādā metodes un destruktori. Piemēri demonstrē, kā no klases izveido objektus, kā arī kā tiek veidota dinamiska atribūtu pievienošana.

> [!NOTE] Klase
> **Klase:** definīcija, kas ietver atribūtus un metodes, un kas attēlo kaut kādu entitāti.

> [!NOTE] Objekts
> **Objekts** – konkrēta klases realizācija, kurā tiek iestatītas noteiktas īpašības un izpildītas metodes.
#### Tēma 2 - Klases izveide
Python valodā ir daudz iebūvētu tipu (piemēram, int, str utt.), ko var izmantot programmās. Tomēr Python arī ļauj definēt savus tipus, izmantojot klases.

>**Klase** attēlo kādu entitāti, un tās konkrēta realizācija (spēcīgā analogija: mūsu priekšstats par cilvēku ar vārdu, vecumu un citām īpašībām) ir **objekts**.

Python valodā klase tiek definēta, izmantojot atslēgas vārdu `class`:
```python
class klases_nosaukums:
    # klases atribūti
    # klases metodes
```

Piemēram, izveidojam vienkāršu klasi:
```python
class Person:
    pass
```

Šajā gadījumā klase Person nosacītā veidā attēlo cilvēku, taču tā nesatur metodes vai atribūtus. Tā vietā tiek izmantots `pass` operators, lai sintaktiski aizpildītu klases ķermeni.

Pēc klases definēšanas varam izveidot tās objektus:

```python
class Person:
    pass

tom = Person()  # definē objekta tom izveidi
bob = Person()  # definē objekta bob izveidi
```

Katram klasē pēc noklusējuma ir konstruktors bez parametriem, ko izsaucot ar `Person()` tiek iegūts jauns Person objekts.
#### Tēma 3 - Konstruktori un atribūti
##### Konstruktori

Lai izveidotu objektu ar sākotnējām vērtībām, mēs definējam konstruktoru kā metodi `__init__()`. Piemērs:

```python
class Person:
    # Konstruktors
    def __init__(self):
        print("Person objekta izveide")

tom = Person()  # izsauc __init__(), kas izdrukā: Person objekta izveide
```

>Konstruktora pirmais parametrs ir `self` – atsauce uz pašreizējo objektu. Python dinamiski nosaka vērtību `self`, tāpēc mums to nav jāievada manuāli.

##### Atribūti

Atribūti glabā objekta stāvokli. Tie tiek definēti konstruktorā, izmantojot `self`:

```python
class Person:
    def __init__(self, name, age):
        self.name = name  # cilvēka vārds
        self.age = age    # cilvēka vecums
 
tom = Person("Tom", 22)
print(tom.name)  # izdrukā: Tom
print(tom.age)   # izdrukā: 22

tom.age = 37
print(tom.age)   # izdrukā: 37
```

Šeit konstruktoram tiek nodoti divi parametri – `name` un `age`, un tie tiek saglabāti kā objekta atribūti. <mark style="background: #ABF7F7A6;">Objekta atribūti var tikt gan nolasīti, gan modificēti pēc objekta izveides.</mark>

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
 
tom = Person("Tom", 22)
tom.company = "Microsoft"
print(tom.company)  # izdrukā: Microsoft
```

>Python’s ļauj mums arī definēt jaunus atributus dinamiski, taču, ja mēģināsim piekļūt tādam atribūtam pirms tā definēšanas, radīsies kļūda.

#### Tēma 4 - Metodes

Klases metodes ir funkcijas, kas nosaka objekta uzvedību. Piemēram:

```python
class Person:
    def say_hello(self):
        print("Hello")
 
tom = Person()
tom.say_hello()  # izdrukā: Hello
```

Pirmais metodes parametrs ir `self`, kas ļauj piekļūt objekta atribūtiem un metodēm. Ja metode pieņem citus parametrus, tie tiek definēti pēc `self` un jānodod izsaukuma laikā:

```python
class Person:
    def say(self, message):
        print(message)
 
tom = Person()
tom.say("Hello METANIT.COM")  # izdrukā: Hello METANIT.COM
```

Lai iekšā metodēs piekļūtu objekta atribūtiem un metodēm, tiek lietots `self`:

```python
self.atribūts    # piekļuve atribūtam
self.metode      # piekļuve metodei
```

Piemērs ar piekļuvi pie laukiem:

```python
class Person:
    def __init__(self, name, age):
        self.name = name  # cilvēka vārds
        self.age = age    # cilvēka vecums
     
    def display_info(self):
        print(f"Name: {self.name}  Age: {self.age}")
 
tom = Person("Tom", 22)
tom.display_info()  # izdrukā: Name: Tom  Age: 22
 
bob = Person("Bob", 43)
bob.display_info()  # izdrukā: Name: Bob  Age: 43
```
#### Tēma 5 - Destruktori

Destruktori ir īpašas metodes (`__del__(self)`), kas izsaucas, kad objekts tiek dzēsts, lai atbrīvotu resursus vai izpildītu nepieciešamās darbības:

```python
class Person:
    def __init__(self, name):
        self.name = name
        print("Izveidots cilvēks ar vārdu", self.name)
     
    def __del__(self):
        print("Dzēsts cilvēks ar vārdu", self.name)
  
tom = Person("Tom")
```

Rezultātā, kad programma beigs darbību, izsauksies destruktors un konsolē tiks izdrukāts:

```
Izveidots cilvēks ar vārdu Tom  
Dzēsts cilvēks ar vārdu Tom
```

Vēl viens piemērs, kur objekts tiek izveidots funkcijā:

```python
class Person:
    def __init__(self, name):
        self.name = name
        print("Izveidots cilvēks ar vārdu", self.name)
     
    def __del__(self):
        print("Dzēsts cilvēks ar vārdu", self.name)
  
def create_person():
    tom = Person("Tom")
     
create_person()
print("Programmas beigas")
```

Šeit objekta dzīves ilgums ir ierobežots funkcijas `create_person` darbības ietvaros – pēc tās izpildes destruktors izsauksies, un konsolē tiks parādīts:

```
Izveidots cilvēks ar vārdu Tom  
Dzēsts cilvēks ar vārdu Tom  
Programmas beigas
```


---
### ⚛ Secinājums/i

- **Klases** definē jaunu tipu ar atribūtiem un metodēm, izmantojot atslēgas vārdu `class`.
- **Objekti** ir konkrētas klases realizācijas ar savu datu stāvokli.
- **Konstruktori** (`__init__`) inicializē objektus ar sākotnējām vērtībām, bet **atribūti** nosaka objekta īpašības.
- **Metodes** apraksta objektu uzvedību un mijiedarbību ar atribūtiem, izmantojot `self`.
- **Dinamiska atribūtu pievienošana** ļauj paplašināt objektus arī pēc to izveides.
- **Destruktori** (`__del__`) tiek izmantoti, lai atbrīvotu resursus, kad objekts vairs nav vajadzīgs. 

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - Python strukturēts]]
Iepriekšēja lapa >>> [[Navigācija - Python OOP]]
Nākama lapa >>> [[Inkapsulācija, atribūti un īpašības]]

---