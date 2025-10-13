___

**Datums:** 2025-10-13
**Laiks:** 13:00
❚ **Tagi:** #kotlin

---
# Map collection

Tas ir vārdnīcu analogs. Dati tiek glabāti `key-value` pāros. Šādi izskatās `Map` izveide:

```kotlin
val solarSystem = mutableMapOf(
    "Mercury" to 0,
    "Venus" to 0,
    "Earth" to 1,
    "Mars" to 2,
    "Jupiter" to 79,
    "Saturn" to 82,
    "Uranus" to 27,
    "Neptune" to 14
)
```

## Map lieluma noteikšana

Lai noteikt kolekcijas lielumu, izmanto funkciju `size`:

```kotlin
println(solarSystem.size)
```

## Elementa pievienošana

Izmantojot `key-value` sintaksi, var peivienot jauno elementu kolekcijai:

```kotlin
solarSystem["Pluto"] = 5
```

## Vērtības modifikācija

Lai mainīt kāda elementa vērtību, izmanto šādu sintaksi:

```kotlin
// Esoša atslēga = jauna vērtība
solarSystem["Jupiter"] = 78
```
## Vērtības nolasīšana

Lai iegūt kādas atslēgas vērtību, izmanto vienu no 2 pieejām:

```kotlin
// Norādi atslēgu
println(solarSystem["Pluto"])
// Izmanto get() funkciju
println(solarSystem.get("Theia"))
```

## `key-value` dzēšana

Lai izdzēst `key-value` pāri no kolekcijas, izmanto funkciju `remove()`, kas saņem atslēgas nosaukumu:

```kotlin
solarSystem.remove("Pluto")
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Sets]]
Nākama lapa >>> [[Navigācija - Collections]]

---