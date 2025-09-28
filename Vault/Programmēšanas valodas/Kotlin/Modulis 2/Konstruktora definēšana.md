___

**Datums:** 2025-09-28
**Laiks:** 12:01
❚ **Tagi:** #kotlin 

---
# Konstruktora definēšana

## Noklusējuma konstruktors

Tas ir konstruktors bez parametriem. To nevajag nekādi aprakstīt, kompilators pats to uzģenerēs.

```kotlin
class SmartDevice {
    ...
}
```

## Primārais konstruktors

Tas ir galvenais konstruktors klasē, deklarēts tieši klases virsrakstā. Bieži izmanto īpašību inicializācijai. Bloks `init` tiek izmantots, lai izpildīt kādu koda fragmentu, kad tiek iniciaizēts/veidots objekts:

```kotlin
class Persona(val vards: String, var vecums: Int) {
    init {
        println("Izveidota persona: $vards, vecums $vecums")
    }
}
```

Var uzrakstīt arī šādi:

```kotlin
class Person constructor(name: String, age: Int) {
    val name: String = name
    var age: Int = age
}
```

![[Pasted image 20250928121837.png]]
## Sekundārais konstruktors

Papildus konstruktori, kas ļauj izveidot objektu ar citu parametru komplektu. Tie **obligāti** izsauc primāro ar `this(...)`.

```kotlin
class Persona(val vards: String) {
    var vecums: Int = 0

    constructor(vards: String, vecums: Int) : this(vards) {
        this.vecums = vecums
    }
}
```

![[Pasted image 20250928121849.png]]
## Objektu veidošana

### Objekta veidošana ar primāro kosntruktoru

Ja izmanto **primāro konstruktoru**, objekts tiek izveidots tieši ar visiem obligātajiem parametriem:

```kotlin
class Persona(val vards: String, var vecums: Int)

fun main() {
    val p1 = Persona("Anna", 25)
    println("${p1.vards}, ${p1.vecums}")
}
```

### Objekta veidošana ar sekundāro kosntruktoru

Ja izmanto **sekundāro konstruktoru**, vari padot papildus argumentus, un objekts tiek inicializēts jau ar citu loģiku.

```kotlin
class Persona(val vards: String) {
    var vecums: Int = 0

    constructor(vards: String, vecums: Int) : this(vards) {
        this.vecums = vecums
    }
}

fun main() {
    val p1 = Persona("Jānis")          // tiek izmantots primārais
    val p2 = Persona("Maija", 30)      // tiek izmantots sekundārais

    println("${p1.vards}, ${p1.vecums}")  // Jānis, 0
    println("${p2.vards}, ${p2.vecums}")  // Maija, 30
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Getteri un setteri]]
Nākama lapa >>> [[Virsklases un apakšklases]]

---