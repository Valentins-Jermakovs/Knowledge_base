___

**Datums:** 2025-09-14
**Laiks:** 12:55
❚ **Tagi:** #java #OOP 

---
### Iterators

Iterators ļauj mums iterēt pa kolekcijām, pirms lieotšanas to ir nepieciešams importēt un pievienot kolekcijai, pa kuru tiek veikta iterēšana.

Iterators atbalsta šādas metodes:

- `next()` - atgriež nākamo elemtu, pārvieto kursoru uz priekšu;
- `hasNext()` - pārbauda, vai priekšā vēl ir elements;
- `remove()` - izdzēš elementu, ko atgrieza pēdējais `next()`.

```java
import java.util.ArrayList;
import java.util.Iterator;

public class IteratorDemo {
    public static void main(String[] args) {
        ArrayList<String> colors = new ArrayList<>();

        colors.add("Red");
        colors.add("Blue");
        colors.add("Green");

        // Получаем итератор
        Iterator<String> it = colors.iterator();

        while (it.hasNext()) {
            String color = it.next();
            System.out.println(color);

            // Удалим "Blue" во время итерации
            if (color.equals("Blue")) {
                it.remove();
            }
        }

        System.out.println("После удаления: " + colors);
    }
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Kārtošana (Sorting List)]]
Nākama lapa >>> [[Navigācija - Modulis 3]]

---