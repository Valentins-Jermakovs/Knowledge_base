___

**Datums:** 2025-09-13
**Laiks:** 19:31
❚ **Tagi:** #java #OOP 

---
### Konstruktori

Konstruktori tiek izmantoti objekta inicializācijai. Konstruktora nosaukums sakrīt ar klases nosaukumu.

**Konstruktora piemērs (ar noklusējuma vērtību, bez parametriem):**

```java
public class Vehicle {

  private String color;
  
  Vehicle() {
     color = "Red";
  }
}
```

**Konstruktora ar parametriem (objekta atribūtu inicializācija):**

```java
public class Vehicle {

  private String color;
  
  Vehicle(String c) {
    color = c;
  }
}
```

**Konstruktora izmantošānas piemērs:**

```java
public class MyClass {
  public static void main(String[ ] args) {
    // Šeit tiek nodots parametrs, iestatīts atribūts
    Vehicle v = new Vehicle("Blue");
  }
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Getters un Setters]]
Nākama lapa >>> [[Vairāki konstruktori]]

---