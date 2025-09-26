___

**Datums:** 2025-09-21
**Laiks:** 12:11
❚ **Tagi:** #kotlin 

---
# Teksta elementu centrēšana un padding

## Kolonnas vertikālā centrēšana

Lai kolonna būtu **vertikāli ekrāna centrā**, izmanto parametru:

```kotlin
verticalArrangement = Arrangement.Center
```

```kotlin
@Composable
fun GreetingText(message: String, from: String, modifier: Modifier = Modifier) {
    Column(
        verticalArrangement = Arrangement.Center,
        modifier = modifier
    ) {
        // ...
    }
}
```

## Padding (atstarpes)

Iekšējas atstarpes no konteinera malām līdz tā saturam:

```kotlin
@Composable
fun GreetingText(message: String, from: String, modifier: Modifier = Modifier) {
    Column(
        verticalArrangement = Arrangement.Center,
        modifier = modifier.padding(8.dp)
    ) {
        // ...
    }
}
```

## Teksta centrēšana horizontāli

`Text()` composable pievieno `textAlign = TextAlign.Center` - teksts centrējas kolonnas platumā:

```kotlin
Text(
    text = message,
    fontSize = 100.sp,
    lineHeight = 116.sp,
    textAlign = TextAlign.Center
)
```

## Paraksta (signature) izkārtojums

Paraksts var būt **pa labi**:

- Piešķir `Modifier.padding()` - iekšējas atstarpes.
- Lieto `.align(Alignment.End)` - izvieto tekstu pa labi.

```kotlin
Text(
    text = from,
    fontSize = 36.sp,
    modifier = Modifier
        .padding(16.dp)
        .align(alignment = Alignment.End)
)
```

### Kopsavilkums

- `Column(verticalArrangement = Arrangement.Center)` → vertikālā centrēšana.
- `modifier.padding(dp)` → atstarpes.
- `TextAlign.Center` → centrē tekstu horizontāli.
- `.align(Alignment.End)` → novieto elementu pa labi.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Teksta elementu izvietošana kolonnā]]
Nākama lapa >>> [[šablons]]

---