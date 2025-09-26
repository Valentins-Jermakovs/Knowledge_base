___

**Datums:** 2025-09-13
**Laiks:** 22:06
❚ **Tagi:** #java #OOP 

---
### Method Overriding

Tas ir tas pats, kas bija parādīts iepriekš, kad apakšklase pārraksta kādu virsklases metodi.

```java
class Animal {
  public void makeSound() {
    System.out.println("Grr...");
  }
}
class Cat extends Animal {
  public void makeSound() {
    System.out.println("Meow");
  }
}
```

```java
public static void main(String[ ] args) {
  Animal b = new Cat();
  
  b.makeSound() // Meow
}
```

Šeit klase `Cat` pārraksta virsklases metodi.

Pāris noteikumu metožu pārrakstīšanai:

- Jābūt ar vienādu atgriešanas tipu un argumentiem;
- Metodi, kas deklarēta kā `final `vai `static`, nevar pārrakstīt;
- Ja metodi nevar mantot, to nevar pārrakstīt;
- Konstruktorus nevar pārrakstīt.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Polimorfisms]]
Nākama lapa >>> [[Programmēšanas valodas/Java (viss)/Java OOP/Modulis 2/Abstraktās klases|Abstraktās klases]]

---