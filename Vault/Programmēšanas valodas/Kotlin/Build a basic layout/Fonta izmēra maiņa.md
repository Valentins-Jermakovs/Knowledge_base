___

**Datums:** 2025-09-21
**Laiks:** 11:30
❚ **Tagi:** #kotlin 

---
# Fonta izmēra maiņa

Teksta izmēra maiņai izmanto `.sp` (scalable pixels). `SP` mainās atbilstoši lietotāja iestatītajam teksta lielumam telefonā. Pēc noklusējuma `SP` = `DP`, bet tas ir elastīgāks tekstam.

## Teksta lieluma maiņa

Lai mainīt teksta izmēru, izmanto atribūtu `fontSize`:

```kotlin
@Composable
fun GreetingText(message: String, modifier: Modifier = Modifier) {
    Text(
        text = message,
        fontSize = 100.sp
    )
}
```

Papildus, lai šī lieta darbotos `.sp`, nepieciešams `import`:

```kotlin
import androidx.compose.ui.unit.sp
```

## Teksta rindu augstuma maiņa

Ja teksts pārklājas, jāpievieno rindu augstums.

```kotlin
@Composable
fun GreetingText(message: String, modifier: Modifier = Modifier) {
    Text(
        text = message,
        fontSize = 100.sp,
        lineHeight = 116.sp
    )
}
```

### Kopsavilkums

- **DP** → izkārtojumam.
- **SP** → fontu izmēram, mainās ar lietotāja iestatījumiem.
- `.sp` jāimportē no `androidx.compose.ui.unit.sp`.
- Papildu parametri:
    - `fontSize` → teksta izmērs.
    - `lineHeight` → atstarpes starp rindām.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Teksta atribūti (izmēra maiņa, rindu augstums)]]
Nākama lapa >>> [[UI hierarhija un elementu izkārtojums]]

---