___

**Datums:** 2025-10-13
**Laiks:** 14:04
❚ **Tagi:** #kotlin 

---
# forEach and string templates with lambdas

Pirmām kārtām mums nepieciešams izveidot `list`, pa kuru iterēsim:

```kotlin
class Cookie(
    val name: String,
    val softBaked: Boolean,
    val hasFilling: Boolean,
    val price: Double
)

val cookies = listOf(
    Cookie(
        name = "Chocolate Chip",
        softBaked = false,
        hasFilling = false,
        price = 1.69
    ),
    Cookie(
        name = "Banana Walnut", 
        softBaked = true, 
        hasFilling = false, 
        price = 1.49
    )...
```

Šādi izskatās `foreach()` lambda funkcijas pieleitojums, tā ļauj iterēt pa šāda saraskta elementiem un kādu no to laukiem:

```kotlin
cookies.forEach {
    println("Menu item: ${it.name}")
}
```

```
Menu item: Chocolate Chip
Menu item: Banana Walnut
Menu item: Vanilla Creme
Menu item: Chocolate Peanut Butter
Menu item: Snickerdoodle
Menu item: Blueberry Tart
Menu item: Sugar and Sprinkles
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - Higher-order functions with collections]]
Nākama lapa >>> [[map funkcija]]

---