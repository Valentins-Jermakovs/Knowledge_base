___

**Datums:** 2025-09-13
**Laiks:** 19:25
❚ **Tagi:** #java #OOP 

---
### Getters un Setters

Tas ir speciālas metodes, kas tiek veidotas, lai iestatīt vai atgriezt atribūtu vērtības.

`getters` - atgriež, nolasa atribūta vērtību;
`setters` - iestata atribūta vērtību.

Re, kā šādas metodes izskatās kodā:

```java
public class Vehicle {

  // Privātais atribūts
  private String color;

  // Getter - atgriež vērtību
  public String getColor() {
    return color;
  }

 // Setter - iestata vērtību
  public void setColor(String c) {
    this.color = c;
  }
}
```

Atslēgvārds `this` norāda šī objekta atribūtu.

Šādi izskatās šo metožu pielietojums `main` blokā:

```java
class Program {
    public static void main(String[ ] args) {
        Vehicle v1 = new Vehicle();
        v1.setColor("Red");
        System.out.println(v1.getColor());
    }
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Programmēšanas valodas/Java (viss)/Java OOP/Modulis 1/Pieejas modifikātori|Pieejas modifikātori]]
Nākama lapa >>> [[Konstruktori]]

---