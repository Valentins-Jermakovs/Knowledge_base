___

**Datums:** 2025-09-14
**Laiks:** 12:03
❚ **Tagi:** #java #OOP 

---
### LinkedList

Gana līdzīgs `ArrayList`.

`Araylist` - vairāk paredzēts datu glabāšanai;
`LinkedList` - vairāk paredzēt biežām manipulāicjām ar datiem.

```java
import java.util.LinkedList;

public class MyClass {
	public static void main (String [] args) {
		LinkedList<String> c = new LinkedList<String>();
		
		c.add("Red");
		c.add("Blue");
		c.add("Green");
		c.add("Orange");
		
		c.remove("Green");
		
		for (String s : c) {
			System.out.println(s);
		}
	}
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[ArrayList]]
Nākama lapa >>> [[HashMap]]

---