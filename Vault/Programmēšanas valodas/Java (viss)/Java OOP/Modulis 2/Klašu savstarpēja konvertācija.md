___

**Datums:** 2025-09-13
**Laiks:** 22:29
❚ **Tagi:** #java #OOP 

---
### Klašu savstarpēja konvertācija

Klašu objektus var konvertēt no apakšklases uz virsklases tipu un otrādi.

Piemērs ar konvertēšanu uz virsklasi:

```java
Animal a = new Cat();
```

Piemērs ar konvertēšanu uz apakšklasi:

```java
Animal a = new Cat();
((Cat)a).makeSound();
```

Vēl viens piemērs ar konvertāciju:

```java
class A {
   public void print() {
      System.out.println("A");
   }
}

class B extends A {
   public void print() {
      System.out.println("B");
   }

   public static void main(String[] args) {
      A object = new B();   // объект типа B, но ссылка типа A
      B b = (B) object;     // явное приведение к B (безопасно, т.к. реально это B)
      b.print();            // вызов метода - B
   }
}

```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Interfeisu pielietojums apakšklasēs]]
Nākama lapa >>> [[Anonīmas klases]]

---