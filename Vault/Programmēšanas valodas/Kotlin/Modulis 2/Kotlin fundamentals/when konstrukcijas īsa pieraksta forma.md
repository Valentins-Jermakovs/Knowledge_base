___

**Datums:** 2025-09-27
**Laiks:** 20:13
❚ **Tagi:** #kotlin 

---
# when konstrukcijas īsa pieraksta forma

Šādi izskatās īsa pieraksta forma:

```kotlin
fun main() {
    val trafficLightColor = "Amber"

    val message = when(trafficLightColor) {
        "Red" -> "Stop"
        "Yellow", "Amber" -> "Slow"
        "Green" -> "Go"
        else -> "Invalid traffic-light color"
    }
    println(message)
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[if, else if, else konstrukciju īsa pieraksta forma]]
Nākama lapa >>> [[null vērtība]]

---