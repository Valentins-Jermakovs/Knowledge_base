___

**Datums:** 2025-10-13
**Laiks:** 12:24
❚ **Tagi:** #kotlin

---
# Lists

`List` tas ir  tāds saraksts, kas tiek izmantots tikai datu glabāšanai un to nolasīšanai.
`MutableList` ir tas pats `List`, bet ar dažādām metodēm datu modifikācijām, piem., elementu pievienošana, dzēšana.

## List

Šadi veido `List` tipa sarakstu:

```kotlin
val solarSystem = listOf("Mercury", "Venus", "Earth", "Mars", "Jupiter", "Saturn", "Uranus", "Neptune")
```

### Piekļūšana pie elementiem

Piekļūt pie elementiem var 2 veidos:

- `[]` norādot indeksu;
- `get()` izmantojot funkciju.

```kotlin
// Indekss
println(solarSystem[2])
// get() funkcija
println(solarSystem.get(3))
```

### Meklējama elementa indeksa noteikšana

Šādi var atrast indeksu meklējama elementam:

```kotlin
// Funkcija indexOf()
println(solarSystem.indexOf("Earth"))
println(solarSystem.indexOf("Pluto"))
```

### Iterācija ar `for` ciklu

Pa saraksta elementiem var izterēt izmantojot `for` ciklu, kas pēc savas būtības līdzīgs `python` ciklam:

```kotlin
for (planet in solarSystem) {
    println(planet)
}
```

## MutableList

Šādi izskatās `MutableList` saraksta izveidošana:

```kotlin
val solarSystem = mutableListOf("Mercury", "Venus", "Earth", "Mars", "Jupiter", "Saturn", "Uranus", "Neptune")
```

### Elementa pievienošana

Lai pievienot elemetnu, tiek izmantota funkcija `add()`. Tā pieņem 1-2 parametrus. Ja norādīts viens parametrs (elements, kas tiek pievienots), elementu pievienos saraksta beigās. Ja norādīts otras parametrs (indekss), elements tiks ievetots norādītā pozīcijā.

```kotlin
solarSystem.add("Pluto")
solarSystem.add(3, "Theia")
```

### Elementa modifikācija

Lai modificēt, mainīt kāda elementa vērtību, izmanto indeksu:

```kotlin
solarSystem[3] = "Future Moon"
```

### Elementa dzēšana

Elementu no saraksta var dzēst norādot tā indeksu vai vērtību:

```kotlin
solarSystem.removeAt(9)
solarSystem.remove("Future Moon")
```

## Pārbaude uz elementa esamību

Pārbaude atgriež `true/false` atkarībā no rezultāta. Pārbaudīt sarasktu uz elementa esamību var 2 veidos:

```kotlin
// Funkcija contains()
println(solarSystem.contains("Pluto"))
// Operators in
println("Future Moon" in solarSystem)
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Arrays]]
Nākama lapa >>> [[Sets]]

---