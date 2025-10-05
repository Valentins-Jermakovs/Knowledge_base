___

**Datums:** 2025-09-13
**Laiks:** 22:00
❚ **Tagi:** #java #OOP 

---
### Polimorfisms

Ļauj vienu funkciju izmantot dažādu tipu objektu apstrādei, savukārt katra šīs funkcijas implementācija darbosies pareizi savam objektam.

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
class Dog extends Animal {
  public void makeSound() {
    System.out.println("Woof");
  }
}
```

Šeit katrai apakšklasei ir sava `makeSound()` funkcija atbilstoši klasei. Ja mēs izveidosim katru šādai apakšklasei objektu, tas atsauksies uz savas klases funkciju, necis uz virsklasi.

```java
public static void main(String[ ] args) {
  Animal a = new Dog();
  Animal b = new Cat();
  
  a.makeSound() // Woof
  b.makeSound() // Meow
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Programmēšanas valodas/Java (viss)/Java OOP/Modulis 2/Mantošana]]
Nākama lapa >>> [[Method Overriding]]

---