___

**Datums:** 2025-09-28
**Laiks:** 12:20
❚ **Tagi:** #kotlin

---
# Virsklases un apakšklases

## Mantošana (Inheritance) Kotlin valodā

**Mantošana** ļauj vienai klasei pārņemt īpašības un funkcijas no citas klases.  
Tas palīdz:

- atkārtoti izmantot kodu,
- sakārtot programmu,
- parādīt, kā klases ir saistītas savā starpā.

 **Piemērs ar viedierīcēm**

Ir dažādas ierīces: **viedtelevizors**, **viedspuldze**, **viedais slēdzis**.  
Visām ir **kopīgas īpašības**: nosaukums, kategorija, statuss.  
Un arī **kopīgas darbības**: ieslēgt / izslēgt.

Bet katrai ierīcei ieslēgšana notiek savādāk:

- Televizoram – jāparāda attēls, jāiestata skaņa un kanāls.
- Spuldzei – tikai jāpalielina spilgtums.

👉 Šādos gadījumos izveido **kopīgu vecāku klasi** ar nosaukumu `SmartDevice`, un katrai ierīcei (`SmartTvDevice`, `SmartLightDevice`) uztaisi **apakšklasi**, kas mantos kopīgo loģiku.

## Virsklases definēšana

```kotlin
open class SmartDevice(val name: String, val category: String) {
    var deviceStatus = "online"

    open fun turnOn() {
        deviceStatus = "on"
    }

    open fun turnOff() {
        deviceStatus = "off"
    }
}
```

`open` nozīmē, ka klasi un metodes drīkst paplašināt. Bez `open` klase ir “noslēgta” un no tās nevar mantot.

## Apakšklases definēšana

`override` nozīmē, ka **mēs pārrakstām vecāku klases metodi**. `super.turnOn()` izsauc vecāku versiju, lai nezaudētu pamatloģiku (piem. statusa maiņu).

**Apakšklase: viedtelevizors**

```kotlin
class SmartTvDevice(deviceName: String, deviceCategory: String) :
    SmartDevice(name = deviceName, category = deviceCategory) {

    var speakerVolume = 2
    var channelNumber = 1

    override fun turnOn() {
        super.turnOn()
        println("$name ieslēgts. Skaļums: $speakerVolume, kanāls: $channelNumber.")
    }

    override fun turnOff() {
        super.turnOff()
        println("$name izslēgts.")
    }
}
```

**Apakšklase: viedspuldze**

```kotlin
class SmartLightDevice(deviceName: String, deviceCategory: String) :
    SmartDevice(name = deviceName, category = deviceCategory) {

    var brightnessLevel = 0

    override fun turnOn() {
        super.turnOn()
        brightnessLevel = 2
        println("$name ieslēgta. Spilgtums: $brightnessLevel.")
    }

    override fun turnOff() {
        super.turnOff()
        brightnessLevel = 0
        println("Spuldze izslēgta.")
    }
}
```

## HAS-A attiecības (kompozīcija)

Ne tikai **“X ir Y” (IS-A)**, bet arī **“X satur Y” (HAS-A)**.  
Piemēram, mājai var būt viedierīces:

```kotlin
class SmartHome(
    val smartTvDevice: SmartTvDevice,
    val smartLightDevice: SmartLightDevice
) {
    fun turnOnTv() = smartTvDevice.turnOn()
    fun turnOffTv() = smartTvDevice.turnOff()

    fun turnOnLight() = smartLightDevice.turnOn()
    fun turnOffLight() = smartLightDevice.turnOff()

    fun turnOffAllDevices() {
        turnOffTv()
        turnOffLight()
    }
}
```

👉 Vienkārši sakot:

- **IS-A (mantošana):** Televizors **ir** viedierīce.
- **HAS-A (kompozīcija):** Māja **satur** viedierīci.

## Polimorfisms

Ja mainīgais ir `SmartDevice`, tas var saturēt gan `SmartTvDevice`, gan `SmartLightDevice`.

```kotlin
fun main() {
    var smartDevice: SmartDevice = SmartTvDevice("Android TV", "Entertainment")
    smartDevice.turnOn()

    smartDevice = SmartLightDevice("Google Light", "Utility")
    smartDevice.turnOn()
}
```

Rezultāts:

```
Android TV ieslēgts. Skaļums: 2, kanāls: 1.
Google Light ieslēgta. Spilgtums: 2.
```

Tas ir **polimorfisms** – viena un tā pati funkcija (`turnOn`) darbojas dažādi atkarībā no objekta tipa.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Konstruktora definēšana]]
Nākama lapa >>> [[Pieejas modifikatori]]

---