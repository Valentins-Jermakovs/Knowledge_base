___

**Datums:** 2025-09-28
**Laiks:** 12:46
❚ **Tagi:** #kotlin

---
# Pieejas modifikatori

|Modifikators|Tajā pašā klasē|Apakšklasē|Tajā pašā modulī|Ārpus moduļa|
|---|---|---|---|---|
|**private**|✔|✘|✘|✘|
|**protected**|✔|✔|✘|✘|
|**internal**|✔|✔|✔|✘|
|**public**|✔|✔|✔|✔|

## Pieejas modifikatori īpašībām (laukiem)

![[Pasted image 20250928125249.png]]

```kotlin
open class SmartDevice(val name: String, val category: String) {

    ...

    private var deviceStatus = "online"

    ...
}
```

## Pieejas modifikatori metodēm

![[Pasted image 20250928125352.png]]

```kotlin
class SmartTvDevice(deviceName: String, deviceCategory: String) :
    SmartDevice(name = deviceName, category = deviceCategory) {

    ...

    protected fun nextChannel() {
        channelNumber++
        println("Channel number increased to $channelNumber.")
    }      

    ...
}
```

## Pieejas modifikatori kosntruktoriem

![[Pasted image 20250928125527.png]]

```kotlin
open class SmartDevice protected constructor (val name: String, val category: String) {

    ...

}
```
## Pieejas modifikatori klasēm

![[Pasted image 20250928125551.png]]

```kotlin
internal open class SmartDevice(val name: String, val category: String) {

    ...

}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Virsklases un apakšklases]]
Nākama lapa >>> [[Īpašību deleģēšana]]

---