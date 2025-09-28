___

**Datums:** 2025-09-28
**Laiks:** 10:43
❚ **Tagi:** #kotlin 

---
# Darbs ar `null` vērtībām

## Metožu izmantošana `?.` operators

Lai izmantot metodes mainīgiem, kas var saturēt `null` vērtības, tiek izmantots operators `?.`:

```kotlin
fun main() {
    var favoriteActor: String? = "Sandra Oh"
    println(favoriteActor?.length)
}
```
## Pārbaude uz `null`

```kotlin
fun main() {
    var favoriteActor: String? = "Sandra Oh"

    if (favoriteActor != null) {
      println("The number of characters in your favorite actor's name is ${favoriteActor.length}.")
    } else {
      println("You didn't input a name.")
    }
}
```
## Pārbaude uz `null` īsa pieraksta forma

```kotlin
fun main() {
    var favoriteActor: String? = "Sandra Oh"

    val lengthOfName = if (favoriteActor != null) {
      favoriteActor.length
    } else {
      0
    }

    println("The number of characters in your favorite actor's name is $lengthOfName.")
}
```

## Elvis operators `?:`

![[Pasted image 20250928104508.png]]

```kotlin
fun main() {
    var favoriteActor: String? = "Sandra Oh"

    val lengthOfName = favoriteActor?.length ?: 0

    println("The number of characters in your favorite actor's name is $lengthOfName.")
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[null vērtība]]
Nākama lapa >>> [[Navigācija - Kotlin fundamentals]]

---