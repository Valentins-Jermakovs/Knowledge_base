___

**Datums:** 2025-09-28
**Laiks:** 13:54
❚ **Tagi:** #kotlin 

---
# `repeat()` funkcija

**Kas ir `repeat()`?**

- `repeat()` ir **higher-order funkcija** – var padot citu funkciju kā argumentu.
- Ļauj vienkārši atkārtot kādu darbību noteiktu reižu skaitu, līdzīgi kā `for` cikls.

Sintakse:

```kotlin
repeat(times: Int, action: (Int) -> Unit)
```

- **times** – cik reizes izpildīt darbību
- **action** – lambda, kas saņem skaitli (0, 1, 2…) un neko neatgriež (`Unit`)

Piemērs ar `trickOrTreat()`

```kotlin
fun main() {
    val treatFunction = trickOrTreat(false) { "$it quarters" }
    val trickFunction = trickOrTreat(true, null)

    repeat(4) {
        treatFunction()   // izpilda 4 reizes
    }

    trickFunction()       // izpilda vienreiz
}
```

Rezultāts:

```
5 quarters
Have a treat!
Have a treat!
Have a treat!
Have a treat!
No treats!
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Lambda izteikumi ar īso sintaksi]]
Nākama lapa >>> [[Navigācija - Kotlin fundamentals]]

---