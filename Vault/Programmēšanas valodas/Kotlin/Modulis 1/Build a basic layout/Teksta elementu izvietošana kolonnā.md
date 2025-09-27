___

**Datums:** 2025-09-21
**Laiks:** 12:04
❚ **Tagi:** #kotlin

---
# Teksta elementu izvietošana kolonnā

- **Row** → elementi blakus horizontāli.
- **Column** → elementi zem cita vertikāli.
- Ja gribas, lai paziņojums (`message`) un paraksts (`from`) būtu katrs savā rindā, jāizmanto **Column**.

```kotlin
@Composable
fun GreetingText(message: String, from: String, modifier: Modifier = Modifier) {
    Column {
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

![[Pasted image 20250921120653.png]]
## Labākā prakse – nodot `modifier`

Lai kolonna būtu elastīga un varētu kontrolēt tās uzvedību/layout, jānodod `modifier` parametrs.

```kotlin
@Composable
fun GreetingText(message: String, from: String, modifier: Modifier = Modifier) {
    Column(modifier = modifier) {
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

### Kopsavilkums

- **Column** → sakārto bērnelementus vertikāli.
- Lieto `modifier = modifier`, lai nodrošinātu atkārtotu izmantošanu un izkārtojuma kontroli.
- Šis risinājums padara **sveicienu** un **parakstu** vizuāli atdalītus un salasāmus.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Teksta elementu izvietošana rindā]]
Nākama lapa >>> [[Teksta elementu centrēšana un padding]]

---