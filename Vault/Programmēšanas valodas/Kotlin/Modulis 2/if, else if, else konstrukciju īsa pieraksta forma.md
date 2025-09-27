___

**Datums:** 2025-09-27
**Laiks:** 20:11
❚ **Tagi:** #kotlin 

---
# `if, else if, else` konstrukciju īsa pieraksta forma

Šādi izskatās īsa pieraksta forma:

```kotlin
fun main() {
    val trafficLightColor = "Black"

    val message = 
      if (trafficLightColor == "Red") "Stop"
      else if (trafficLightColor == "Yellow") "Slow"
      else if (trafficLightColor == "Green") "Go"
      else "Invalid traffic-light color"

    println(message)
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[when konstrukcija]]
Nākama lapa >>> [[when konstrukcijas īsa pieraksta forma]]

---