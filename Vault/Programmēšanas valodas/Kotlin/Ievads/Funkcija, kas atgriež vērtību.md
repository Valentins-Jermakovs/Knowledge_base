___

**Datums:** 2025-09-17
**Laiks:** 22:12
❚ **Tagi:** #kotlin 

---
### Funkcija, kas atgriež vērtību

Šādi jāraksta funkcijas, kas atgriež kādu vērtību:

```kotlin
fun birthdayGreeting(): String {
    val nameGreeting = "Happy Birthday, Rover!"
    val ageGreeting = "You are now 5 years old!"
    return "$nameGreeting\n$ageGreeting"
}
```

Ja funkcija neko neatgriež, tad tiek izmantots atslēgvārds `Unit`:

```kotlin
fun birthdayGreeting(): Unit {
    println("Happy Birthday, Rover!")
    println("You are now 5 years old!")
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Programmēšanas valodas/Kotlin/Ievads/Komentāri|Komentāri]]
Nākama lapa >>> [[Funkcija ar parametru]]

---