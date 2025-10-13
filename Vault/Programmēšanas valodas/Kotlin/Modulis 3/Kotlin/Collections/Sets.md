___

**Datums:** 2025-10-13
**Laiks:** 12:50
❚ **Tagi:** #kotlin

---
# Sets

Sets tas ir tāds kolekcijas tips, kas satur tikai unikālus elementus. Šādi izskatās tā veidošana:

```kotlin
val solarSystem = mutableSetOf("Mercury", "Venus", "Earth", "Mars", "Jupiter", "Saturn", "Uranus", "Neptune")
```

## Kolekcijas lieluma noteikšana

Lai noteikt, cik elementu satur `sets`, izmnato funkciju `size`:

```kotlin
// 8
println(solarSystem.size)
```

## Elementa pievienošana

Lai pievienot elementu, izmanto funkciju `add()`, kas šajā gadījumā pieņem tikai vienu parametru:

```kotlin
solarSystem.add("Pluto")
```

## Pārbaude uz elementa esamību

Lai pārbaudīt, vai `setā` pastāv meklējamais elements, izmanto funkciju `contains()`:

```kotlin
println(solarSystem.contains("Pluto"))
```

## Elementa dzēšana

Lai izdzēst elementu, izmanto funkciju `remove()`:

```kotlin
solarSystem.remove("Pluto")
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Lists un MutableList]]
Nākama lapa >>> [[Map collection]]

---