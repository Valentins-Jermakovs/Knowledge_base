___

**Datums:** 2025-09-14
**Laiks:** 12:38
❚ **Tagi:** #java #OOP 

---
### HashSet

Komplekti var saturēt tikai unikālos elementus.

```java
import java.util.HashSet;

public class MyClass{
	public static void main(String [] args) {
		HashSet<String> set = new HashSet<String>();
		
		set.add("A");
		set.add("B");
		set.add("C");
		
		System.out.println(set);
	}
}
```

Metode `size()` ļāuj uzzināt komplekta garumu.

*Piezīme. HashSet nesaglabā elementu kārtību, to dara tā analogs LinkedHashSet.*

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[HashMap]]
Nākama lapa >>> [[Kārtošana (Sorting List)]]

---