___

**Datums:** 2025-10-08
**Laiks:** 11:18
❚ **Tagi:** #kotlin 

---
# Switcher

Switch ir interfeisa elements, kas ļauj lietotājam iestatīt to uz `true` vai `false` vērtību.

Šādi tas izskatās kodā:

```kotlin
Switch(
            modifier = modifier
                .fillMaxWidth()
                .wrapContentWidth(Alignment.End),
            checked = roundUp,
            onCheckedChange = onRoundUpChanged,
        )
```

Šeit ir daži parametri:

- `modifier` - atbild par konteineria uzvedību un ārējo izskatu;
- `checked` - šeit `switch` sagaida mainīgo
- `onCheckedChange` - šeit sagaida `lamba` funkciju.

`Switch` elementa pielietojum programmā, sākumā nepieciešams apskatīt visu `Compose` elementa koda fragmentu:

```kotlin
@Composable
fun RoundTheTipRow(
    roundUp: Boolean,
    onRoundUpChanged: (Boolean) -> Unit,
    modifier: Modifier = Modifier)
{
    Row(
        modifier = modifier
            .fillMaxWidth()
            .size(48.dp),
        verticalAlignment = Alignment.CenterVertically
    ) {
        Text(text = stringResource(R.string.round_up_tip))
        Switch(
            modifier = modifier
                .fillMaxWidth()
                .wrapContentWidth(Alignment.End),
            checked = roundUp,
            onCheckedChange = onRoundUpChanged,
        )

    }
}
```

Darbības princips ir samēra vienkāršs, kā minēts iepriekš, tiek sagaidīts mainīgais un `lambda` funkcija.

Un tagad pati programma:

*Mainīgo bloks:*

```kotlin
@Composable
fun TipTimeLayout() {
    var roundUp by remember { mutableStateOf(false) }
```

Šeit tiek izveidots mainīgais, kas saglabā sevī `switch` pozīciju, vai tas esot `true` vai `false`.

*Elementa izsaukšana programmas ķermenī:*

```kotlin
RoundTheTipRow(
            roundUp = roundUp,
            onRoundUpChanged = { roundUp = it },
            modifier = Modifier.padding(bottom = 32.dp)
        )
```

Šet tiek nodota funkcija un caur `lamba` tiek norādīts, ka veicot izmaiņas, tas ir, pārvietojot `switch` uz `true`, `false`, tiek pārrakstīts nodotais mainīgais.

*Funkcija, kas sagaida `switch` vērtību:*

```kotlin
private fun calculateTip( amount: Double, tipPercent: Double = 15.0, roundUp: Boolean): String
{
    var tip = tipPercent / 100 * amount
    if (roundUp) {
        tip = kotlin.math.ceil(tip)
    }

    return NumberFormat.getCurrencyInstance().format(tip)
}
```

Ja `switch` ir uz `true`, tiek veikta  rezultāta noapaļošana.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Programma tip-calculator]]
Nākama lapa >>> [[ScrollVertical]]

---