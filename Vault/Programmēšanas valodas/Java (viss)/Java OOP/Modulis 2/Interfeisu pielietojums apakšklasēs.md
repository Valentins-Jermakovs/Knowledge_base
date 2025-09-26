___

**Datums:** 2025-09-13
**Laiks:** 22:23
❚ **Tagi:** #java #OOP 

---
### Interfeisu pielietojums apakšklasēs

Lai apakšklase varētu mantot interfeisu, izmanto atslēgvārdu `implements`:

```java
interface Animal {
	public void eat();
	public void makeSound();
}

public class Cat implements Animal {
	public void eat() {
		System.out.println("omnomnom");
	}
	public void makeSound() {
		System.out.println("Meow");
	}
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Interfeisi ievads]]
Nākama lapa >>> [[Klašu savstarpēja konvertācija]]

---