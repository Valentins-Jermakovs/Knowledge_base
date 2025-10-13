___

**Datums:** 2025-10-12
**Laiks:** 15:53
❚ **Tagi:** #kotlin 

---
# Enum klases

Enum klases tiek izmantotas, lai glabāt sevī kādus nemaināmus datus, to sarakstu. Piemēram, nedēļas dienas vai mēnešu nosaukumi.

Šādi veido `enum` tipa klasi:

```kotlin
enum class Difficulty {
    EASY, MEDIUM, HARD
}
```

Izveidosim arī `generic` klasi:

```kotlin
class Question<T>(
    val questionText: String,
    val answer: T,
    // Pielietojam enum klasi
    // Norādam to kā datu tipu
    val difficulty: Difficulty
)
```

Un šādi izskatās `enum` klases pielietojums citās klasēs:

```kotlin
val question1 = Question<String>("Quoth the raven ___", "nevermore", Difficulty.MEDIUM)
val question2 = Question<Boolean>("The sky is green. True or false", false, Difficulty.EASY)
val question3 = Question<Int>("How many days are there between full moons?", 28, Difficulty.HARD)
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Generic klases]]
Nākama lapa >>> [[Data klases]]

---