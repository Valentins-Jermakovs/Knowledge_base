___

**Datums:** 2025-09-21
**Laiks:** 12:01
❚ **Tagi:** #kotlin 

---
# Teksta elementu izvietošana rindā

Ja vienkārši pievieno vairākus `Text()` elementus, tie var pārklāties. Lai to novērstu, elementus jāievieto **Row composable**, kas izvieto bērnelementus horizontāli blakus.

```kotlin
@Composable
fun GreetingText(message: String, from: String, modifier: Modifier = Modifier) {
    Row {
        Text(
            text = message,
            fontSize = 100.sp,
            lineHeight = 116.sp,
        )
        Text(
            text = from,
            fontSize = 36.sp
        )
    }
}
```

![[Pasted image 20250921120249.png]]

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[UI hierarhija un elementu izkārtojums]]
Nākama lapa >>> [[Teksta elementu izvietošana kolonnā]]

---