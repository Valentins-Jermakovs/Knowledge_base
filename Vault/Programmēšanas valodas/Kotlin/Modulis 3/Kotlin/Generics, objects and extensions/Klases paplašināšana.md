___

**Datums:** 2025-10-12
**Laiks:** 17:06
❚ **Tagi:** #kotlin

---
# Klases paplašināšana

## Īpašība

Klasi var paplašināt ar īpašībām (get, set) un metodēm.

```kotlin
val Quiz.StudentProgress.progressText: String
    get() = "${answered} of ${total} answered"
```

Obligāti jānorāda datu tipu.

```kotlin
fun main() {
    println(Quiz.progressText)
}
```

Datu iegūšanas piemers.

## Funkcija

Šādi izskatās jaunās funkcijas pievienošana.

```kotlin
fun Quiz.StudentProgress.printProgressBar() {
    repeat(Quiz.answered) { print("▓") }
    repeat(Quiz.total - Quiz.answered) { print("▒") }
    println()
    println(Quiz.progressText)
}
```

Un šādi to izmanto:

```kotlin
fun main() {
    Quiz.printProgressBar()
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Objekts kompanjons]]
Nākama lapa >>> [[Interfeisi]]

---