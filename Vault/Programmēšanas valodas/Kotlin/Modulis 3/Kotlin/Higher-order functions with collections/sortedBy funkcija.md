___

**Datums:** 2025-10-13
**Laiks:** 14:42
❚ **Tagi:** #kotlin

---
# sortedBy() funkcija

Šī funkcija tiek izmantota, lai kārtot kolekciju elementus. Piemērs ar `cookies`:

```kotlin
val alphabeticalMenu = cookies.sortedBy {
    it.name // norādam lauku, pa kuru kārtot
}
```

Veicam izvadu:

```kotlin
println("Alphabetical menu:")
alphabeticalMenu.forEach {
    println(it.name)
}
/*
	Alphabetical menu:
	Banana Walnut
	Blueberry Tart
	Chocolate Chip
	Chocolate Peanut Butter
	Snickerdoodle
	Sugar and Sprinkles
	Vanilla Creme
*/
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[fold funkcija]]
Nākama lapa >>> [[Navigācija - Higher-order functions with collections]]

---