___

**Datums:** 2025-10-13
**Laiks:** 14:13
❚ **Tagi:** #kotlin

---
# map() funkcija

`map()` funkcija ļauj uz kādas kolekcijas pamata izveidot citu kolekciju. Piemēram, iepriekš tika veidota kolekcija `coockies`, šeit mēs izveidosim jauno kolekciju, kas saturēs tikai `string` datus un elementu nosaukumu un cenu:

```kotlin
val fullMenu = cookies.map {
    "${it.name} - $${it.price}"
}
```

Šeit `$$` pirmais simbols tiek uztverts kā dollāra zīme.
Un iterējam pa jauno kolekciju izmantojot `foreach()` funkciju:

```kotlin
println("Full menu:")
fullMenu.forEach {
    println(it)
}
```

```
Full menu:
Chocolate Chip - $1.69
Banana Walnut - $1.49
Vanilla Creme - $1.59
Chocolate Peanut Butter - $1.49
Snickerdoodle - $1.39
Blueberry Tart - $1.79
Sugar and Sprinkles - $1.39
```
 
---
### ⇄ Saistības

Iepriekšēja lapa >>> [[forEach and string templates with lambdas]]
Nākama lapa >>> [[filter funkcija]]

---