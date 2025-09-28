___

**Datums:** 2025-09-28
**Laiks:** 13:26
❚ **Tagi:** #kotlin 

---
# Funkcijas ieraksts mainīgā

Funkciju var ierakstīt mainīgā izmantojot 2 pieraksta veidus:

- standarta;
- lambda.

## Standarta funkcijas ieraksts mainīga

```kotlin
fun main() {
    val trickFunction = ::trick
}

fun trick() {
    println("No treats!")
}
```

## Lambda ieraksts

Galvena atšķirība, kā šeit neitiek izmantots `::` operators un funkciju raksta bez `()` apaļām iekavām, tās aizvieto ar `=` vienādības zīmi:

```kotlin
fun main() {
    val trickFunction = trick
    trick()
    trickFunction()
}

val trick = {
    println("No treats!")
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - Kotlin fundamentals]]
Nākama lapa >>> [[Funkcija kā datu tips]]

---