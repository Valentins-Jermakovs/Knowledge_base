___

**Datums:** 2025-09-27
**Laiks:** 20:00
❚ **Tagi:** #kotlin 

---
# if...else if...else

Šeit viss tāpat kā citās valodās:

```kotlin
fun main() {
    val trafficLightColor = "Black"

    if (trafficLightColor == "Red") {
        println("Stop")
    } else if (trafficLightColor == "Yellow") {
        println("Slow")
    } else if (trafficLightColor == "Green") {
        println("Go")
    } else {
        println("Invalid traffic-light color")
    }

}
```

**Salīdzināšanas operatori:**

| Operators | Skaidrojums         |
| --------- | ------------------- |
| ==        | vienāds             |
| !=        | nav vienāds         |
| >         | lielāks             |
| <         | mazāks              |
| >=        | lielāks vai vienāds |
| <=        | mazāks vai vienāds  |

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - Kotlin fundamentals]]
Nākama lapa >>> [[when konstrukcija]]

---