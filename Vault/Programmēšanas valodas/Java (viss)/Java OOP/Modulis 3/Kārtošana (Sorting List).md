___

**Datums:** 2025-09-14
**Laiks:** 12:46
❚ **Tagi:** #java #OOP 

---
### Kārtošana (Sorting List)

Lai kārtot sarakstus, vajag importēt klasi `Collections`:

```java
import java.utils.ArrayList;
import java.utils.Collections;

public class MyClass{
	public static void main(String [] args) {
		ArrayList<String> animals = new ArrayList<String>();
		
		animals.add("tiger");
		animals.add("cat");
		animals.add("snake");
		animals.add("dog");
		
		Collections.sort(animals);
		
		System.out.println(animals);
	}
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[HashSet]]
Nākama lapa >>> [[Iterators]]

---