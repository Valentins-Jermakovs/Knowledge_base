___

**Datums:** 2025-10-12
**Laiks:** 17:14
❚ **Tagi:** #kotlin

---
# Interfeisi

Ja klase manto interfeisu, tai vajag implementēt visas interfeisa īpašības un metodes.

Šādi izskatās interfeisa definēšana:

```kotlin
interface ProgressPrintable {
    val progressText: String
    fun printProgressBar()
}
```

Šādi izskatās interfeisa mantošana:

```kotlin
class Quiz : ProgressPrintable {
    ... 
}
```

Lai realizēt interfeisa īpašības un metodes, izmanto atslēgvārdu `override`:

```kotlin
class Quiz : ProgressPrintable {
	// Īpašība
	override val progressText: String
        get() = "${answered} of ${total} answered"
    // Metode
    override fun printProgressBar() {
	    repeat(Quiz.answered) { print("▓") }
	    repeat(Quiz.total - Quiz.answered) { print("▒") }
	    println()
	    println(progressText)
	}
}
```

Pārrakstītu īpašību un metožu izmantošanas piemērs:

```kotlin
fun main() {
    Quiz().printProgressBar()
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Klases paplašināšana]]
Nākama lapa >>> [[Scope funkcijas]]

---