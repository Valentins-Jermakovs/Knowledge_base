___

**Datums:** 2025-09-13
**Laiks:** 22:15
❚ **Tagi:** #java #OOP 

---
### Abstraktās klases

Tas ir tādas klases, kas satur abstraktās metodes. Abstraktās metodes nav realizētas šajās klasēs. Abstrakto klašu mērķis ir aprakstīt ideju. Visām apakšklasēm, kas manto abstrakto klasi, jārealizē abstraktās klases metodes.

Abstraktās klases piemērs:

```java
abstract class Animal {
  int legs = 0;
  public abstract void makeSound();
}
```

Piemērs ar apakšklasi, kas manto abstrakto klasi:

```java
public class Cat extends Animal {
	public void makeSound() {
		System.out.println("Meow") // Realizēta abstraktā metode
	}
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Method Overriding]]
Nākama lapa >>> [[Interfeisi ievads]]

---