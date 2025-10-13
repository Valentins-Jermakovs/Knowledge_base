___

**Datums:** 2025-10-13
**Laiks:** 14:18
❚ **Tagi:** #kotlin

---
# `filter()` funkcija

Šī funkcija ļauj veidot kolekciju apakškolekcijas izmantojot dažādus nosacījumus priekš filtrācijas. Piemēram, mums vajag kolekciju, kur būs tikai `softbaked` tipa cepumi:

```kotlin
val softBakedMenu = cookies.filter {
    it.softBaked
}
```

Veiksim izvadu:

```kotlin
println("Soft cookies:")
softBakedMenu.forEach {
    println("${it.name} - $${it.price}")
}
```

```
Soft cookies:
Banana Walnut - $1.49
Snickerdoodle - $1.39
Blueberry Tart - $1.79
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[map funkcija]]
Nākama lapa >>> [[groupBy funkcija]]

---