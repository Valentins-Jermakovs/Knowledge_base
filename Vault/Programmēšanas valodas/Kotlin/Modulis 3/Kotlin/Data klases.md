___

**Datums:** 2025-10-12
**Laiks:** 16:13
❚ **Tagi:** #kotlin

---
# Data klases

Šīs klases tiek izmantotas, lai glabāt datus, nekādas loģikas tās nesatur. Šādi izskatāš `data` klases veidošana:

```kotlin
data class Question<T>(
    val questionText: String,
    val answer: T,
    val difficulty: Difficulty
)
```

Šādas klases var vienkārši izvadīt konsolē, salīdzināt un veikt objektu kopijas.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Enum klases]]
Nākama lapa >>> [[Singleton objekts]]

---