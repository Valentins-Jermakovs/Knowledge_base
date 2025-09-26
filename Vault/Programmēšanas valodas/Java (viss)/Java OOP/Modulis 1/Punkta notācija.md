___

**Datums:** 2025-09-13
**Laiks:** 19:05
❚ **Tagi:** #java #OOP 

---
### Punkta notācija

Caur `.` punktu, var iestatīt objektam **atribūtus** un izmantot **metodes**:

```java
public class Vehicle {
    int maxSpeed;
    int wheels;
    String color;
    double fuelCapacity;  
    
    void horn() {
        System.out.println("Beep!");
    }
}

class MyClass {
    public static void main(String[ ] args) {
        Vehicle v1 = new Vehicle();
        Vehicle v2 = new Vehicle();
        v1.color = "red";
        v2.horn();
    }
}
```

Atribūtus var iestatīt pat bez konstruktora.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Klases atribūti]]
Nākama lapa >>> [[Programmēšanas valodas/Java (viss)/Java OOP/Modulis 1/Pieejas modifikātori|Pieejas modifikātori]]

---