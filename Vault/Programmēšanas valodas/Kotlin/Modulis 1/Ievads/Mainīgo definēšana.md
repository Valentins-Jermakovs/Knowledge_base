___

**Datums:** 2025-09-17
**Laiks:** 21:31
❚ **Tagi:** #kotlin 

---
### Mainīgo definēšana

![[14c69d3231012a14_1440.png]]


> [!NOTE] Pievērs uzmanību!
> `val` - konstante, vērtība nevar tikt mainīga.
> `var` - vērtību var mainīt.


Šādi izskatās mainīgo definēšana un izmantošana konsoles izvadā:

```kotlin
fun main() {
    val numberOfPhotos: Int = 100
    val photosDeleted: Int = 10
    println("$numberOfPhotos photos")
    println("$photosDeleted photos deleted")
    println("${numberOfPhotos - photosDeleted} photos left")
}
```

Lai izvadīt kādu mainīgo konsolē, pirms tā ieliec `$` simbolu. Ja gribi veikt skaitļošanu, tad ievieto mainīgos `${}` figūriekavās.

```kotlin
fun main() {
    var cartTotal: Int = 0
    cartTotal = 20
    println("Total: $cartTotal")
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Programmēšanas valodas/Kotlin/Modulis 1/Ievads/Datu tipi|Datu tipi]]
Nākama lapa >>> [[Inkrementa, dekrementa operatori]]

---