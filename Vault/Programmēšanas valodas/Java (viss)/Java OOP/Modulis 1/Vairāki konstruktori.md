___

**Datums:** 2025-09-13
**Laiks:** 19:38
❚ **Tagi:** #java #OOP 

---
### Vairāki konstruktori

Vienai klasei var būt vairāki konstruktori. šeit piemēram ir 1 konstruktors bez parametriem un 1 kosntruktors ar parametru:

```java
public class Vehicle {
    private String color;
    
    Vehicle() { // Pirmais konstruktors
        this.setColor("Red");
    }
    Vehicle(String c) { // Otrais konstruktors
        this.setColor(c);
    }
    
    // Setter
    public void setColor(String c) {
        this.color = c;
    }
    
    // Getter
    public String getColor() {
        return color;
    }
}
```

Šādi izskatās objekta inicializācija klasei ar vairākiem kosntruktoriem:

```java
public class Program {
    public static void main(String[] args) {        
        //color will be "Red" - Konstruktors bez parametriem
        Vehicle v1 = new Vehicle();
        
        //color will be "Green" - Konstruktors ar parametru
        Vehicle v2 = new Vehicle("Green"); 
        
        System.out.println(v2.getColor());
    }
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Konstruktori]]
Nākama lapa >>> [[Static atribūti]]

---