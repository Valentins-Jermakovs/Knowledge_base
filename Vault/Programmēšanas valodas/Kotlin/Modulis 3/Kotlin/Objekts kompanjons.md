___

**Datums:** 2025-10-12
**Laiks:** 16:26
❚ **Tagi:** #kotlin 

---
# Objekts kompanjons

Tu vari definēt `singletone` objektus citās klasēs, padarot to par objektu kompanjonu un piekļūt pie tā laukiem, metodēm izmantojot punkta notāciju:

```kotlin
class Quiz {
    val question1 = Question<String>("Quoth the raven ___", "nevermore", Difficulty.MEDIUM)
    val question2 = Question<Boolean>("The sky is green. True or false", false, Difficulty.EASY)
    val question3 = Question<Int>("How many days are there between full moons?", 28, Difficulty.HARD)

    companion object StudentProgress {
        var total: Int = 10
        var answered: Int = 3
    }
}

```

`companion` padara objektu par kompanjonu. Piemērs, kā piekļut pie kompanjona klases laukiem, metodēm:

```kotlin
fun main() {
    println("${Quiz.answered} of ${Quiz.total} answered.")
}
```

Norādi virsklases nosaukumu!

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Singleton objekts]]
Nākama lapa >>> [[Klases paplašināšana]]

---