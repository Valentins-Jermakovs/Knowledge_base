___

**Datums:** 2025-10-12
**Laiks:** 17:22
❚ **Tagi:** #kotlin 

---
# Scope funkcijas

## let()

`let()` funkcija ļauj piekļūt pie objekta datiem nenorādot tā nosaukumu:

```kotlin
fun printQuiz() {
    question1.let {
        println(it.questionText)
        println(it.answer)
        println(it.difficulty)
    }
    println()
    question2.let {
        println(it.questionText)
        println(it.answer)
        println(it.difficulty)
    }
    println()
    question3.let {
        println(it.questionText)
        println(it.answer)
        println(it.difficulty)
    }
    println()
}
```

## apply()

`apply()` funkcija, ļauj izsaukt objekta metodes, bez paša objekta izveides.

Tradicionāli mēs veidojam klases eksemplāru šādi:

```kotlin
val quiz = Quiz()
quiz.printQuiz()
```

Taču funkcija `apply()` ļauj mums izveidot objektu un izsaukt tā metodes bez saglabāšanas mainīgā:

```kotlin
Quiz().apply {
    printQuiz()
}
```

`Quiz()` - klases nosaukums. `{}` figūriekavās apraksta visas klases metodes, ko jāizpilda. Šāds objekts eksistē tikai izsaukuma laikā.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Interfeisi]]
Nākama lapa >>> [[šablons]]

---