___

**Datums:** 2025-09-14
**Laiks:** 12:10
❚ **Tagi:** #java #OOP 

---
### HashMap

HasMap tiek izmantoti, lai glabāt datus kolekcijās, `key-value` pāros.

```java
import java.util.HashMap;

public class MyClass{
	public static void main(String [] args) {
		HashMap<String, Integer> points = new HashMap<String, Integer>();
		
		points.put("Amy", 154);
		points.put("Dave", 42);
		points.put("Rob", 85);
		
		System.out.println(points.get("Dave"));
	}
}
```

Metodes:

- `put()` - pievienot ierakstu;
- `remove()` - dzēst ierakstu;
- `get()` - nolasīt vērtību;
- `containsKey()` - atgriež `null`, ja neatrod;
- `containsValue()` - atgriež `null`, ja neatrod.

HashMap ļauj pievienot tikai jaunas, unikālas atslēgas. Ja tu pievienosi jau eksistējošu atslēgu, `Java` parrākstīs esošas atslēgas vērtību.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[LinkedList]]
Nākama lapa >>> [[HashSet]]

---