___

**Datums:** 2025-10-12
**Laiks:** 15:49
❚ **Tagi:** #kotlin 

---
# Generic klases

Tas ir tādas klases, kas ļauj iestatīt kāda klases lauka datu tipu caur parametru objekta veidošanas laikā.

```kotlin
// Generic klase
class Question<T>(
    val questionText: String,
    val answer: T,
    val difficulty: String
)
```

Šādi izskatās tādas klases objekta veidošana:

```kotlin
fun main() {
    val question1 = Question<String>("Quoth the raven ___", "nevermore", "medium")
    val question2 = Question<Boolean>("The sky is green. True or false", false, "easy")
    val question3 = Question<Int>("How many days are there between full moons?", 28, "hard")
}
```

`<>` - šajās iekavās tiek norādīts datu tips.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - Generics, objects and extensions]]
Nākama lapa >>> [[Enum klases]]

---