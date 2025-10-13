___

**Datums:** 2025-10-12
**Laiks:** 16:22
❚ **Tagi:** #kotlin 

---
# Singleton objekts

Tas ir tādsa klases, kurām var eksistēt tikai viens vienīgais objekts.  Šādam klasēm nav konstruktora, objektu inicializē klases veidošanas laikā:

```kotlin
object StudentProgress {
    var total: Int = 10
    var answered: Int = 3
}
```

Lai piekļūt pie šāda objekta laukiem, metodēm, izmanto punkta notāciju:

```kotlin
fun main() {
    ...
    println("${StudentProgress.answered} of ${StudentProgress.total} answered.")
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Data klases]]
Nākama lapa >>> [[Objekts kompanjons]]

---