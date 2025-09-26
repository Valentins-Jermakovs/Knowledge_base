___

**Datums:** 2025-09-13
**Laiks:** 20:02
❚ **Tagi:** #java #OOP 

---
### Static metodes

Tā pat kā `static` atribūti, `static` metodes var tikt izsauktas bez objekta:

```java
public class Vehicle {
  public static void horn() {
    System.out.println("Beep");
  }
}

public class MyApp {
	public static void main(String [] args) {
			
		Vehicle.horn();
	}
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Static metodes]]
Nākama lapa >>> [[packages]]

---