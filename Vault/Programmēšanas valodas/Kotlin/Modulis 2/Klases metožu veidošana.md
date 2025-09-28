___

**Datums:** 2025-09-28
**Laiks:** 11:46
❚ **Tagi:** #kotlin 

---
# Klases metožu veidošana

Šādi veido klases metodes:

```kotlin
class SmartDevice {
    fun turnOn() {
        println("Smart device is turned on.")
    }

    fun turnOff() {
        println("Smart device is turned off.")
    }
}
```

# Klases metožu izsaukšana

![[Pasted image 20250928114845.png]]

Un šādi var izsaukt objektam klases metodes:

```kotlin
fun main() {
    val smartTvDevice = SmartDevice()
    smartTvDevice.turnOn()
    smartTvDevice.turnOff()
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Klases eksemplāra veidošana]]
Nākama lapa >>> [[Klases īpašību (lauku) veidošana]]

---