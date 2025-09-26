___

**Datums:** 2025-09-13
**Laiks:** 22:36
❚ **Tagi:** #java #OOP 

---
### Anonīmas klases

Anonīmas klases ļauj pārrakstīt kādas klases metodi objekta inicializācijas laikā.

Pieņemsim, kā mums ir klase `Machine`:

```java
class Machine {
  public void start() {
    System.out.println("Starting...");
  }
}
```

Kad mēs veidojam klases `Machine` objektu, varam pārrakstīt `start` metodi, izmantojot atslēgvārdu `@Override`:

```java
class Program{
	public static void main(String [] args) {
		Machine car = new Machine() {
			@Override public void start() {
				System.out.println("Woooo");
			};
		}
		car.start;
	}
}
```

Šāda pārrakstīšana darbojas tikai uz vienu, konkrētu objektu, šeit tas ir `car`. Tas nozīmē, kā citi klases `Machine` objekti saturēs nemainītu metodi `start`.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Klašu savstarpēja konvertācija]]
Nākama lapa >>> [[Ieliktas klases (Inner Classes)]]

---