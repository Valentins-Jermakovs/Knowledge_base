___

**Datums:** 2025-09-28
**Laiks:** 11:50
❚ **Tagi:** #kotlin 

---
# Klases īpašību (lauku) veidošana

Šādi veido klases īpašības:

```kotlin
class SmartDevice {

    val name = "Android TV"
    val category = "Entertainment"
    var deviceStatus = "online"

    fun turnOn() {
        println("Smart device is turned on.")
    }

    fun turnOff() {
        println("Smart device is turned off.")
    }
}
```

Tā kā šeit īpašībām nav uzlikti klašu modifikatori, tie ir viegli pieejami, cau punktu `.`:

```kotlin
fun main() {
    val smartTvDevice = SmartDevice()
    println("Device name is: ${smartTvDevice.name}")
    smartTvDevice.turnOn()
    smartTvDevice.turnOff()
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Klases metožu veidošana]]
Nākama lapa >>> [[Getteri un setteri]]

---