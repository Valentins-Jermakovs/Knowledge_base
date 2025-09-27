___

**Datums:** 2025-09-27
**Laiks:** 18:40
❚ **Tagi:** #kotlin 

---
# Modifier


> [!NOTE] Modifier
> `Modifier` ir tas, kas ļauj kontrolēt **izmērus, pozīciju, fonu, klikšķus un citus vizuālos efektus** visam komponentam (konteinerim), nevis tikai tekstam vai attēlam.

Kas ir `Modifier`?

- Tas ir **objekts**, ko pievieno **katrā Compose elementā**;
- Ar to mēs sakam: “kā šis elements izskatīsies un kā uzvedīsies”;
- Modifier varam ķēdēt.

```kotlin
Box(
    modifier = Modifier
        .size(100.dp)            // platums un augstums
        .background(Color.Blue)  // fons
        .padding(8.dp)           // iekšējie atstarpes
        .border(2.dp, Color.Red) // apmale
)
```

**Biežāk lietotie `Modifier` parametri**

| Funkcija               | Ko dara                                                    |
| ---------------------- | ---------------------------------------------------------- |
| `size(width, height)`  | Nosaka platumu un augstumu                                 |
| `fillMaxWidth()`       | Izstiepj elementu pa visu platumu                          |
| `fillMaxHeight()`      | Izstiepj elementu pa visu augstumu                         |
| `background(color)`    | Nosaka fona krāsu                                          |
| `padding(dp)`          | Iekšējie margi                                             |
| `border(width, color)` | Apmale                                                     |
| `clip(shape)`          | Noapaļo malas, forma (piem., `CircleShape`)                |
| `clickable {}`         | Padara elementu klikšķojamu                                |
| `offset(x, y)`         | Pārvieto elementu pa X un Y                                |
| `align(alignment)`     | Līdzināšana konteinerī (`TopStart`, `Center`, `BottomEnd`) |
| `weight(n)`            | Svarīgums Row/Column, kā elementi dalīs vietu              |

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Attēla noformēšana]]
Nākama lapa >>> [[Box konteineris]]

---