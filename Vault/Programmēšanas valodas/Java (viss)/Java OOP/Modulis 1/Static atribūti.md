___

**Datums:** 2025-09-13
**Laiks:** 19:57
❚ **Tagi:** #java #OOP 

---
### Static

Atribūti ar `static` modifikātoru ir tādi atribūti, kas raksturīgi visai klasei, nevis konkrētam klases objektam. Var pateikt kā tas esot tāds ka globāls atribūts visiem objektiem.

```java
public class Counter {
	public static int COUNT = 0;
	
	public Counter() {
		COUNT++;
	}
}

public class MyApp {
	public static void main(String [] args) {
		Counter c1 = new Counter();
		Counter c2 = new Counter();
		
		System.out.println(Counter.COUNT); // 2
	}
}
```

*Piezīme. Šādi atribūti var būt izsaukti bez objekta. Piemērā parādīts klasesNosaukums.staticAtribūts*

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Vairāki konstruktori]]
Nākama lapa >>> [[Static metodes]]

---