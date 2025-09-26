⏲ **Datums:** 2025-04-28   
⏲ **Laiks:** 16:42 
❚ **Tagi:**  #OOP 
⌬ **Objekts:**  `OOP`

---
### ⬢ Detalizēts apraksts
#### Tēma 1 - Ievads

Abstraktās bāzes klases ļauj definēt metožu “līgumus” klasēm, kuras tās mantos, nodrošinot, ka visas obligātās metodes tiek implementētas. Moduļi un paketes palīdz loģiski organizēt Python kodu un izvairīties no nosaukumu konfliktiem.

> [!NOTE] Abstraktā klase
> Klase, kurā var būt abstraktas (nenodrošinātas) metodes, kuras obligāti jārealizē apakšklasēm.

> [!NOTE] @abstractmethod
> Dekors, kas atzīmē metodi par abstraktu.

> [!NOTE] Modulis
> Atsevišķs *.py* fails, kas satur klases, funkcijas, mainīgos.

#### Tēma 2 - Abstraktā klase

Abstraktā klase ir tāda klase,  kas manto `abc.ABC` un var saturēt metodes bez implementācijas.

```python
# Šis nepieciešsams, lai izveidot abstrakto klasi
from abc import ABC, abstractmethod

# Abstraktā klase
class Animal(ABC):
    
    @abstractmethod # Obligāti realizējama apakšklasēs
    def make_sound(self):
        pass

# Mēģinot uztaisīt objektu tieši no Animal, būs kļūda
# animal = Animal()  # Šis izsauks TypeError

# Konkrēta (sub) klase / apakšklase
class Dog(Animal):
    
    def make_sound(self):
        return "Vau vau!"

class Cat(Animal):
    
    def make_sound(self):
        return "Miau!"

# Tagad var izveidot objektus no konkrētām klasēm
dog = Dog()
cat = Cat()

print(dog.make_sound())  # Rezultāts: Vau vau!
print(cat.make_sound())  # Rezultāts: Miau!
```
#### Tēma 4 - Abstraktā klase ar vairākām metodēm

```python
from abc import ABC, abstractmethod

class Drawable(ABC):
    @abstractmethod
    def draw(self):
        #Zīmē objektu.
        pass

    @abstractmethod
    def resize(self, scale: float):
        #Maina objekta mērogu.
        pass

    @abstractmethod
    def move(self, x: float, y: float):
        #Pārvieto objektu uz koordinātām (x, y).
        pass
```

---
### ⚛ Secinājums/i

Python izmanto abstraktās bāzes klases, lai definētu obligātās metodes, ko jārealizē apakšklasēm.

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Asociācija, salikums un apvienojums Python]]
Nākama lapa >>> [[Navigācija - Python OOP]]
Nākama lapa >>> [[Navigācija - Python strukturēts]]

---