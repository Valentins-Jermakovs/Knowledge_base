⏲ **Datums:** 2025-04-28   
⏲ **Laiks:** 08:57 
❚ **Tagi:**  #OOP 

⌬ **Objekts:**  `OOP`

---
### ⬢ Detalizēts apraksts
#### Tēma 1 - Ievads

Šis materiāls demonstrē, kā Python klasēs pēc noklusējuma atribūti ir publiski pieejami, kā arī kā definēt privātus atribūtus, izmantojot dubultas apakšsvītras `("__")`Turpmāk tiek izskaidrota gan inkapsulācijas nozīme, gan metodes (getteri un setteri), gan īpašību (properties) izmantošana, lai nodrošinātu drošu piekļuvi objekta datiem.

> [!NOTE] Inkapsulācija
> Objektorientētās programmēšanas pamatprincips, kas paredz iekšējā datu slēpšanu un ārējās piekļuves ierobežošanu, lai novērstu nevēlamas modifikācijas.

> [!NOTE] Privātie atribūti
> Atribūti, kuru nosaukums sākas ar dubultām apakšsvītrām, piemēram, `__name`, un kuri ārpus klases ir nepieejami, jo Python tos noslēpj speciālā nosaukumā (piemēram, `_Person__name`).

> [!NOTE] Īpašības (properties)
> Elegants veids, kā definēt getterus un setterus Python klasēs, izmantojot dekoratorus `@property` un `@<property_name>.setter`, kas ļauj kontrolēt atribūtu vērtību piekļuvi un modificēšanu.
#### Tēma 2 - Noklusējuma publiskums un problēmas

<mark style="background: #ABF7F7A6;">Pēc noklusējuma klasēs definētie atribūti ir publiski pieejami, tas nozīmē, ka no jebkuras programmas daļas var piekļūt un mainīt objekta atribūtus.</mark> Piemēram:

```python
class Person:
    def __init__(self, name, age):
        self.name = name    # iestata vārdu
        self.age = age      # iestata vecumu
                 
    def print_person(self):
        print(f"Vārds: {self.name}\tVecums: {self.age}")
         
 
tom = Person("Tom", 39)
tom.name = "Supercilvēks"   # maina atribūtu name
tom.age = -129             # maina atribūtu age
tom.print_person()         # izdruka: Vārds: Supercilvēks     Vecums: -129
```

Tomēr šāda pieeja ļauj piešķirt neatbilstošas vērtības, piemēram, negatīvu vecumu, kas bieži ir nevēlams.
#### Tēma 3 - Inkapsulācija un privāti atribūti

<mark style="background: #ABF7F7A6;">Lai ierobežotu tiešu piekļuvi atribūtiem, Python ļauj definēt privātus atribūtus, kuru nosaukums sākas ar divām apakšsvītrām.</mark> Piemēram, pārrakstīsim augšējā piemēru, padarot abus atribūtus - `name` un `age` - privātus:

```python
class Person:
    def __init__(self, name, age):
        self.__name = name    # iestata vārdu (privāts)
        self.__age = age      # iestata vecumu (privāts)
                  
    def print_person(self):
        print(f"Vārds: {self.__name}\tVecums: {self.__age}")
          
 
tom = Person("Tom", 39)
tom.__name = "Supercilvēks"  # mēģina mainīt atribūtu __name
tom.__age = -129             # mēģina mainīt atribūtu __age
tom.print_person()           # izdruka: Vārds: Tom        Vecums: 39
```

Šajā gadījumā, pat ja mēģinām mainīt `tom.__name` un `tom.__age`, izsaucot `print_person()` redzam, ka vērtības joprojām paliek nemainīgas – tie ir klases iekšējie privātie atribūti, kas reāli tiek glabāti kā `_Person__name` un `_Person__age`.

Lai gan ir iespējams piekļūt privātiem atribūtiem, izmantojot to pilno nosaukumu (piem., `tom._Person__name`).
#### Tēma 4 - getteri un setteri, īpašības

Lai kontrolētu piekļuvi privātajiem atribūtiem, tiek izmantotas speciālas piekļuves metodes – getteri un setteri. Piemēram:

```python
class Person:
    def __init__(self, name, age):
        self.__name = name    # iestata vārdu
        self.__age = age      # iestata vecumu
 
    # Setteris vecumam ar pārbaudi
    def set_age(self, age):
        if 0 < age < 110:
            self.__age = age
        else:
            print("Nepieņemams vecums")
 
    # Getters vecumam
    def get_age(self):
        return self.__age
 
    # Getters vārdam
    def get_name(self):
        return self.__name
     
    def print_person(self):
        print(f"Vārds: {self.__name}\tVecums: {self.__age}")
          
 
tom = Person("Tom", 39)
tom.print_person()   # izdruka: Vārds: Tom  Vecums: 39
tom.set_age(-3486)   # izdruka: Nepieņemams vecums
tom.set_age(25)
tom.print_person()   # izdruka: Vārds: Tom  Vecums: 25
```

>Ar šo metožu palīdzību mēs varam droši nolasīt un modificēt privātos atribūtus, ieviešot papildus loģiku vērtību validācijai.

Python piedāvā vēl elegantāku pieeju – īpašības (properties), izmantojot dekoratorus `@property` un `@<property_name>.setter`. Piemērs ar īpašību izmantošanu:

```python
class Person:
    def __init__(self, name, age):
        self.__name = name    # iestata vārdu
        self.__age = age      # iestata vecumu
 
    # Getters īpašībai age
    @property
    def age(self):
        return self.__age
    # Setteris īpašībai age
    @age.setter
    def age(self, age):
        if 0 < age < 110:
            self.__age = age
        else:
            print("Nepieņemams vecums")
 
    # Tikai getters īpašībai name – tāpēc, name tikai nolasāms
    @property
    def name(self):
        return self.__name
     
    def print_person(self):
        print(f"Vārds: {self.__name}\tVecums: {self.__age}")
          
 
tom = Person("Tom", 39)
tom.print_person()   # izdruka: Vārds: Tom  Vecums: 39
tom.age = -3486      # izdruka: Nepieņemams vecums (setteris)
print(tom.age)       # izdruka: 39 (getters)
tom.age = 25         # setteris atjauno vecumu uz 25
tom.print_person()   # izdruka: Vārds: Tom  Vecums: 25
```

Ar īpašībām mēs varam piekļūt gan getteriem, gan setteriem, izmantojot vienkāršu notāciju `tom.age` gan nolasīšanai, gan iestatīšanai. Ja īpašībai ir definēts tikai getters (piemēram, `name`), tās vērtību nevar mainīt ārpus klases.

---
### ⚛ Secinājums/i

- **Pēc noklusējuma** klases atribūti ir publiski pieejami, kas var radīt datu drošības problēmas.
- **Privātie atribūti** tiek definēti ar dubultām apakšsvītrām (`__name`) un aizsargā objektu no nevēlamas ārējas manipulācijas.
- **Getteri un setteri** ļauj kontrolēt piekļuvi un validēt atribūtu vērtības.
- **Īpašības (properties)** nodrošina elegantāku piekļuves kontroli, apvienojot getterus un setterus vienkāršā atribūtu piekļuves sintaksē.  

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Kā izveidot klasi Python]]
Nākama lapa >>> [[Mantošana Python]]

---