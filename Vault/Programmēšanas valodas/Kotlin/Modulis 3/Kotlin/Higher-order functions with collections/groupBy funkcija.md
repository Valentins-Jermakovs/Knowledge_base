___

**Datums:** 2025-10-13
**Laiks:** 14:24
❚ **Tagi:** #kotlin

---
# groupBy() funkcija

Šī metode ļāuj izveidot no saraksta `map` tipa kolekcijas, kur `key` būs kāds rezultāts un tā `values` būs vērtības, saraskta elementi, kas tika filtrēti:

```kotlin
val groupedMenu = cookies.groupBy { it.softBaked }
```

Šeit mēs izveidojam `map` kolekciju, kurā eksistē 2 atslēgas `tru, false` un pie katras savs cepumu veids.

```kotlin
val softBakedMenu = groupedMenu[true] ?: listOf()
val crunchyMenu = groupedMenu[false] ?: listOf()
```

Šeit mēs saglabājam katru veidu atsevišķi, tiek pielietots `?:` operators, jo atslēgas var būt tukšas. Veicam izvadu:

```kotlin
println("Soft cookies:")
softBakedMenu.forEach {
    println("${it.name} - $${it.price}")
}
println("Crunchy cookies:")
crunchyMenu.forEach {
    println("${it.name} - $${it.price}")
}
```

```
Soft cookies:
Banana Walnut - $1.49
Snickerdoodle - $1.39
Blueberry Tart - $1.79
Crunchy cookies:
Chocolate Chip - $1.69
Vanilla Creme - $1.59
Chocolate Peanut Butter - $1.49
Sugar and Sprinkles - $1.39
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[filter funkcija]]
Nākama lapa >>> [[fold funkcija]]

---