___

**Datums:** 2025-09-14
**Laiks:** 11:40
❚ **Tagi:** #java #OOP 

---
### Threads

Threads (поток). `Java` valoda var vienlaikus palaist vairākas komponentes. Lai izveidot `Thread` komponenti, paplašini klasi un apraksti metodi `run()`:

```java
class Loader extends Thread{
	public void run(){
		System.out.println("Hello!");
	}
}
```

Šādi izskatīsies galvenais programmas bloks:

```java
class MyClass{
	public static void main(String [] args) {
		Loader object = new Loader();
		object.start(); // Hello!
	}
}
```

Kā redzams, metode `start()` darbina metodi `run()`.

> [!NOTE] Threads prioritātes
> Threadiem ir prioritātes līmeņi, no 1 līdz 10, pēc noklusejuma visiem ir 5. Lai mianīt prioritāti, izmanto metodi `setPriority()`.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Kļūdu apstrāde]]
Nākama lapa >>> [[ArrayList]]

---