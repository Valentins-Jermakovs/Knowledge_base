___

**Datums:** 2025-09-21
**Laiks:** 11:24
❚ **Tagi:** #kotlin 

---
### Teksta elementa pievienošana

`GreetingText()` ir Composable funkcija, kas **parāda tekstu ekrānā**. Tā izmanto **`Text()` Composable** (elementu, lai parādīt tekstu).

```kotlin
@Composable
fun GreetingText(message: String, modifier: Modifier = Modifier) {
    Text(
        text = message
    )
}
```

Parametri:
- `message: String` → nosaka, kāds teksts būs redzams.
- `modifier: Modifier` → nodrošina elastību UI pielāgošanai (stils, novietojums, izmēri u.c.).

Lai redzēt šīs funkcijas grafisko izvadu, tiek izmantots `@Preview`:

```kotlin
@Preview(showBackground = true)
@Composable
fun BirthdayCardPreview() {
    HappyBirthdayTheme {
        GreetingText(message = "Happy Birthday Sam!")
    }
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Example of a composable function]]
Nākama lapa >>> [[Fonta izmēra maiņa]]

---