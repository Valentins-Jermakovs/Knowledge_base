___

**Datums:** 2025-09-14
**Laiks:** 11:08
❚ **Tagi:** #java #OOP 

---
### Ieliktas klases

Klsaes var būt ieliktas viena otrā, kā `if..else` nosacījumi:

```java
public class Robot{
	int id;
	
	public Robot(int id) {
		this.id = id;
		Brainb b = new Brain();
		b.think();
	}
	
	private class Brain{
		public void think() {
			System.out.println(id "is thinking...");
		}
	}
}
```

Šeit klasei `Robot` ir iekšēja klase `Brain`, kurai ir pieeja pie visiem klases `Robot` atribūtiem un metodēm.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Anonīmas klases]]
Nākama lapa >>> [[Enums]]

---