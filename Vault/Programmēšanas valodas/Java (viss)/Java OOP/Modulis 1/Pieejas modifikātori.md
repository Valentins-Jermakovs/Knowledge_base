___

**Datums:** 2025-09-13
**Laiks:** 19:08
❚ **Tagi:** #java #OOP 

---
### Pieejas modifikātori

Klasēm ir šādi pieejas modifikatori:

- `public` - klase ir pieejama citās klasēs;
- `default` - klase ir pieejama tikai tām klasēm, kas atrodas vienā pakā.

Atribūtiem un metodēm ir pieejami šādi pieejas modifikātori:

- `default` - bez modifikātora, ir pieejama tikai tām klasēm, kas atrodas vienā pakā;
- `public` - pieejams jebkurai citai klasei;
- `protected` - pieejams tikai pašas klases un apakšklasu ietvaru, kas manto virsklasi;
- `private` - pieejams tikai pašai klasei, kurā ir veidots.

Piemērs ar pieejas modifikatoru izmantošanu:

```java
public class Vehicle {

  // Šie atribūti ir pieejami tikai pašas klases ietvaros
  private int maxSpeed;
  private int wheels;
  private String color;
  private double fuelCapacity;

  // Šī metode ir pieejam citām klasēm
  public void horn() {
    System.out.println("Beep!");
  }
}
```


> [!NOTE] Labā prakse
> Labā prakse ir turēt visus klases atribūtus `private`, slēgtus citām klasēm.


---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Punkta notācija]]
Nākama lapa >>> [[Getters un Setters]]

---