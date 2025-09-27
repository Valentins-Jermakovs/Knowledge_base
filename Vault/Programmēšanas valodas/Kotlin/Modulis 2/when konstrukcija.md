___

**Datums:** 2025-09-27
**Laiks:** 20:04
❚ **Tagi:** #kotlin 

---
# `when` konstrukcija

Tas ir analogs `switch` kosntrukcijai, tikai šeit pastāv savas atšķirības un īpatnības:

```kotlin
fun main() {
    val trafficLightColor = "Amber"

    when (trafficLightColor) {
        "Red" -> println("Stop")
        "Yellow", "Amber" -> println("Slow")
        "Green" -> println("Go")
        else -> println("Invalid traffic-light color")
    }
}
```

Taču šeit vēl var veidot pat diapazonus un noteikt datu tipu:

```kotlin
fun main() {
    val x: Any = 20

    when (x) {
        2, 3, 5, 7 -> println("x is a prime number between 1 and 10.")
        in 1..10 -> println("x is a number between 1 and 10, but not a prime number.")
        is Int -> println("x is an integer number, but not between 1 and 10.")
        else -> println("x isn't an integer number.")
    }
}
```

`Any`  ļauj izveidot objektu, mainīgo bez noteikta datu tipa, un jau konstrukcijā `when` var veikt ar to turpmākas darbības.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[if...else if...else]]
Nākama lapa >>> [[if, else if, else konstrukciju īsa pieraksta forma]]

---