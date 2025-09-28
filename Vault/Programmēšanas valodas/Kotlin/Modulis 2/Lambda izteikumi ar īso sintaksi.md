___

**Datums:** 2025-09-28
**Laiks:** 13:47
❚ **Tagi:** #kotlin 

---
# Lambda izteikumi ar īso sintaksi

## Parametra nosaukuma izlaide

```kotlin
// parastā versija
val coins: (Int) -> String = { quantity -> "$quantity quarters" }

// īsā versija
val coins: (Int) -> String = { "$it quarters" }
```

## Lambda tieši kā arguments

Lambda var padot tieši funkcijai, neglabājot to mainīgajā.

```kotlin
val treatFunction = trickOrTreat(false, { "$it quarters" })
val trickFunction = trickOrTreat(true, null)

treatFunction()
trickFunction()
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Funkcija kā datu tips]]
Nākama lapa >>> [[repeat() funkcija]]

---