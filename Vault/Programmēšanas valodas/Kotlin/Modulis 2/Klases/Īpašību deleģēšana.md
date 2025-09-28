___

**Datums:** 2025-09-28
**Laiks:** 13:03
❚ **Tagi:** #kotlin

---
# Īpašību deleģēšana

**Kas ir deleģēšana (delegates)?**

Parasti īpašībai (`var`) vajag **backing field** (`field`) un savu `get` / `set` kodu.  
Ja vairākām īpašībām loģika ir vienāda, piemēram:

- pārbaudīt vērtības robežas,
- ierobežot diapazonu,

-- tad tas jāraksta vairākas reizes. Tas nav ērti.

👉 Kotlin piedāvā **deleģēšanu** – tu pasaki, lai īpašības vērtības pārvaldību izdara cita klase.

## Bez deleģēšanas (dublēts kods)

```kotlin
class Light {
    var brightness: Int = 0
        set(value) {
            if (value in 0..100) {
                field = value
            }
        }
}
```

Šeit `brightness` īpašībai pārbaudām, vai vērtība ir no 0 līdz 100.  
Ja būtu vēl 3 īpašības ar līdzīgu pārbaudi, būtu jāatkārto viss `set`.
## Ar deleģēšanu

Mēs izveidojam vienu **palīgklasi**, kas dara šo darbu par mums.

```kotlin
import kotlin.properties.ReadWriteProperty
import kotlin.reflect.KProperty

class RangeRegulator(
    initialValue: Int,
    private val min: Int,
    private val max: Int
) : ReadWriteProperty<Any?, Int> {

    private var fieldData = initialValue

    override fun getValue(thisRef: Any?, property: KProperty<*>): Int {
        return fieldData
    }

    override fun setValue(thisRef: Any?, property: KProperty<*>, value: Int) {
        if (value in min..max) {
            fieldData = value
        }
    }
}
```

Tagad īpašība izmanto **deleģētāju** ar `by`:

```kotlin
class Light {
    var brightness by RangeRegulator(initialValue = 0, min = 0, max = 100)
}
```

**Bez deleģēšanas:** katrai īpašībai raksti `get`/`set`.
**Ar deleģēšanu:** īpašība pati neko nezina, visu darbu izdara palīgklase (`RangeRegulator`).

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Īpašību deleģēšana]]
Nākama lapa >>> [[Navigācija - Kotlin fundamentals]]

---