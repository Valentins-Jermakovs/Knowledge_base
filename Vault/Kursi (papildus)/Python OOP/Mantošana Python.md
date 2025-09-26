⏲ **Datums:** 2025-04-28   
⏲ **Laiks:** 09:09 
❚ **Tagi:** #OOP

⌬ **Objekts:**  `OOP`

---
### ⬢ Detalizēts apraksts
#### Tēma 1 - Ievads

Mantošana ļauj izveidot jaunu klasi, balstoties uz jau esošu klasi. Kopā ar inkapsulāciju mantojums ir viens no fundamentālajiem objektorientētās programmēšanas akmeņiem. Mantojuma būtība slēpjas tādu jēdzienu kā apakšklase un augšklase (bāzes klase) izmantošanā. Apakšklase manto no augšklases visas publiskās īpašības un metodes. Augšklase tiek saukta arī par bāzes vai vecāku klasi, bet apakšklase – par mantoto, izrietošu vai bērnu klasi.

> [!NOTE] Mantošana
> Mehānisms, kas ļauj izveidot jaunu klasi, kas manto visu publisko īpašību un metožu kopumu no citas klases.

> [!NOTE] Augšklase un apakšklase
> **Augšklase (bāzes klase, vecāku klase):** klase, no kuras tiek mantotas īpašības un metodes;
> **Apakšklase (mantotā klase, bērnu klase):** klase, kura manto no augšklases.

> [!NOTE] Daudzmantojums
> Īpašība, kas ļauj vienai klasei mantot no vairākiem augšklases, taču ar iespējamu metožu konfliktu.
#### Tēma 2 - Vienkārša mantošana

Mantošana ļauj izveidot jaunu klasi, balstoties uz jau esošu klasi. 
Piemēram, mums ir klase Person, kas attēlo cilvēku:

```python
class Person:
 
    def __init__(self, name):
        self.__name = name   # cilvēka vārds
 
    @property
    def name(self):
        return self.__name
     
    def display_info(self):
        print(f"Name: {self.__name} ")
```

Pieņemsim, ka mums nepieciešama klase darbiniekam, kas strādā kādā uzņēmumā. Tā kā darbinieks ir cilvēks, lai nepārrakstītu kopēju funkcionalitāti, izmantojam mantošanu:

```python
class Employee(Person):
 
    def work(self):
        print(f"{self.name} works")
 
 
tom = Employee("Tom")
print(tom.name)     # izdrukā: Tom
tom.display_info()  # izdrukā: Name: Tom 
tom.work()          # izdrukā: Tom works
```

>Klase Employee pilnībā pārņem Person funkcionalitāti un tikai pievieno metodi work().
>Uzmanību jāvelta tam, ka privātie atribūti, piemēram, `__name`, nav pieejami apakšklasē
>(vienmēr jāizmanto publiskie interfeisi, piemēram, property).
#### Tēma 3 - Daudzmantojums

Python atbalsta daudzmantojumu – vienai klasei var mantot no vairākiem augšklasēm. Piemēram:

```python
# Klase darbinieks
class Employee:
    def work(self):
        print("Employee works")
  
# Klase students
class Student:
    def study(self):
        print("Student studies")
  
  
class WorkingStudent(Employee, Student):  # WorkingStudent manto no Employee un Student
    pass
  
  
tom = WorkingStudent()
tom.work()      # izdrukā: Employee works
tom.study()     # izdrukā: Student studies
```

<mark style="background: #ABF7F7A6;">Šeit klase WorkingStudent nesatur nekādu papildus funkcionalitāti, bet manto gan no Employee, gan no Student, tādējādi objekts var izpildīt abu klašu metodes.</mark>
#### Tēma 4 - Matošanas detalizēts piemērs

Ja klasēm Employee un Student ir sarežģītāks funkcionalitātes kopums, varam definēt mantojumu šādi:

```python
class Employee:
 
    def __init__(self, name):
        self.__name = name
 
    @property
    def name(self):
        return self.__name
 
    def work(self):
        print(f"{self.name} works")
 
 
class Student:
 
    def __init__(self, name):
        self.__name = name
 
    @property
    def name(self):
        return self.__name
 
    def study(self):
        print(f"{self.name} studies")
 
 
class WorkingStudent(Employee, Student):
    pass
 
 
tom = WorkingStudent("Tom")
tom.work()      # izdrukā: Tom works
tom.study()     # izdrukā: Tom studies
```

Šeit, izmantojot daudzmantojumu, klase WorkingStudent manto īpašības un metodes no Employee un Student. Tomēr jāņem vērā, ka, ja bāzes klasēs ir identiski vai konfliktējoši nosaukumi, izpildes kārtība var radīt neskaidrības.
#### Tēma 5 - Sarežģītāks piemērs ar apakšklašu laukiem un to metodēm
```python
class Employee:
    def __init__(self, name, job):
        self.name = name  # Darbinieka vārds
        self.job = job    # Darba amata nosaukums

    def work(self):
        print(f"{self.name} strādā kā {self.job}")

    def change_job(self, new_job):
        self.job = new_job  # Metode, lai mainītu darba amatu


class Student:
    def __init__(self, name, subject):
        self.name = name        # Studenta vārds
        self.subject = subject  # Priekšmets, ko studē students

    def study(self):
        print(f"{self.name} studē {self.subject}")

    def change_subject(self, new_subject):
        self.subject = new_subject  # Metode, lai mainītu priekšmetu


class WorkingStudent(Employee, Student):
    def __init__(self, name, job, subject):
        # Izsaucam __init__ no vecāku klasēm Employee un Student
        Employee.__init__(self, name, job)
        Student.__init__(self, name, subject)

    def work_and_study(self):
        self.work()  # Izsauc work metodi no Employee
        self.study()  # Izsauc study metodi no Student


# Izveidojam objektu WorkingStudent
ws = WorkingStudent("Tom", "Izstrādātājs", "Python")

# Izvadām informāciju par darbu un mācībām
ws.work()   # Tom strādā kā Izstrādātājs
ws.study()  # Tom studē Python

# Mainām darba amatu un priekšmetu
ws.change_job("Sistēmu analītiķis")
ws.change_subject("JavaScript")

# Atkal izvadām, lai redzētu izmaiņas
ws.work()   # Tom strādā kā Sistēmu analītiķis
ws.study()  # Tom studē JavaScript

# Izsaucam metodi, kas izpilda gan darbu, gan mācības
ws.work_and_study()
# Izvade:
# Tom strādā kā Sistēmu analītiķis
# Tom studē JavaScript
```

Šajā piemērā ir trīs klases: `Employee`, `Student` un `WorkingStudent`. 
- Klase `Employee` attēlo darbinieku ar vārdu un darba amatu, kā arī piedāvā iespēju mainīt darba amatu. 
- Klase `Student` attēlo studentu ar vārdu un priekšmetu, kuru viņš studē, un ļauj mainīt priekšmetu. 
- Klase `WorkingStudent` ir apvienojums no abām iepriekšējām klasēm, ļaujot gan strādāt, gan studēt vienlaikus. 

Katra klase satur metodes, kas ļauj manipulēt ar tās īpašībām, piemēram, mainīt darba amatu vai studiju priekšmetu.

---
### ⚛ Secinājums/i

Mantošana ļauj izveidot jaunu klasi, pamatojoties uz esošu klasi, kurā apakšklase manto visas publiskās īpašības un metodes no augšklases, paplašinot vai modificējot funkcionalitāti. Daudzmantojums nodrošina iespēju vienai klasei mantot no vairākiem augšklasēm, taču tas prasa rūpīgu metožu izšķiršanu, jo konflikt-situācijas var rasties, ja vairākām augšklasēm ir metodes ar vienādiem nosaukumiem.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Inkapsulācija, atribūti un īpašības]]
Nākama lapa >>> [[Asociācija, salikums un apvienojums Python]]

---