___

**Datums:** 2025-09-28
**Laiks:** 13:33
❚ **Tagi:** #kotlin 

---
# Funkcija kā datu tips

Funkciju var izmantot kā datu tipu.
Sintakse: `(parametru_tipi) -> atgriežamais_tips`

Piemēri:
- `() -> Unit` – funkcija bez parametriem, neko neatgriež.
- `(Int, Int) -> Int` – funkcija ar 2 `Int` parametriem, atgriež `Int`.

## Funkcija kā mainīgais

```kotlin
val trick: () -> Unit = {
    println("No treats!")
}

val treat: () -> Unit = {
    println("Have a treat!")
}

fun main() {
    trick()
    treat()
}
```

## Funkcija kā atgriežamais tips

Funkcija var atgriezt citu funkciju.

```kotlin
fun trickOrTreat(isTrick: Boolean): () -> Unit {
    if (isTrick) return trick
    else return treat
}

fun main() {
    val f1 = trickOrTreat(false)
    val f2 = trickOrTreat(true)
    f1()
    f2()
}
```

## Funkcija kā parametrs

Funkciju var padot citai funkcijai kā argumentu.

```kotlin
fun trickOrTreat(isTrick: Boolean, extraTreat: (Int) -> String): () -> Unit {
    if (isTrick) return trick
    else {
        println(extraTreat(5))
        return treat
    }
}

fun main() {
    val coins: (Int) -> String = { qty -> "$qty quarters" }
    val cupcake: (Int) -> String = { "Have a cupcake!" }

    val f1 = trickOrTreat(false, coins)
    val f2 = trickOrTreat(true, cupcake)
    f1()
    f2()
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Funkcijas ieraksts mainīgā]]
Nākama lapa >>> [[Lambda izteikumi ar īso sintaksi]]

---