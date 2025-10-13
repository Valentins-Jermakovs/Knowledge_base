___

**Datums:** 2025-10-13
**Laiks:** 12:16
❚ **Tagi:** #kotlin

---
# Masīvs

Maksmiāls masīva izmērs ir 100 elementi.
## Masīva deklarācija

Pastāv 2 veidi, kā var deklarēt masīvu.

```kotlin
// Ar norādītu datu tipu
val rockPlanets = arrayOf<String>("Mercury", "Venus", "Earth", "Mars")
// Bez norādita datu tipa - kotlin to nosaka automātiski
val gasPlanets = arrayOf("Jupiter", "Saturn", "Uranus", "Neptune")
```

Masīvus var apvienot:

```kotlin
val solarSystem = rockPlanets + gasPlanets
```

## Piekļūšana pec indeksa

Izmantojot `[]` kvadrātiekavas var piekļūt pie masīva elementiem:

```kotlin
println(solarSystem[0])
println(solarSystem[1])
println(solarSystem[2])
println(solarSystem[3])
println(solarSystem[4])
println(solarSystem[5])
println(solarSystem[6])
println(solarSystem[7])
```

## Elementa vērtības maiņa

Norādot indeksu var mainīt masīva elementa vērtību:

```kotlin
solarSystem[3] = "Little Earth"
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - Collections]]
Nākama lapa >>> [[Lists un MutableList]]

---