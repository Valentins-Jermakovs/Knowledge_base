___

**Datums:** 2025-09-14
**Laiks:** 11:54
❚ **Tagi:** #java #OOP 

---
### ArrayList

`Java API` sniedz piedāvā `ArrayList`, speciālo klasi, lai glabāt objektus un manipulēt ar objektu grupām.

```java
import java.util.ArrayList;
//...
ArrayList colors = new ArrayList();
```

Šādam objektam var manuāli norādīt ietilpību:

```java
ArrayList<String> colors = new ArrayList<String>(10);
```

`<datuTips>` - šādās iekavās norādi objekta datu tipu.

Tas ir kā dinamiskais sarakst, atbalsta šādas metodes:

- `add()` - pievienot norādīto objektu sarakstam;
- `remove()` - izdzēst norādīto objektu no saraksta;
- `contains()` - atgriež `true`, ja saraksts satur norādīto objektu;
- `size()` - atgriež elementu skaitu sarakstā;
- `clear()` - izdzēš visus elementus no saraksta;
- `get()` - atgriež elementu, kas atrodas norādītā pozīcijā, iekavās norādi indeksu.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Threads]]
Nākama lapa >>> [[LinkedList]]

---