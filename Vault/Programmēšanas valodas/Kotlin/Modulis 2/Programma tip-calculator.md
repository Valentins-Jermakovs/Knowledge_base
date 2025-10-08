___

**Datums:** 2025-10-05
**Laiks:** 20:08
❚ **Tagi:** #kotlin 

---
# Programma tip-calculator

## TextField komponente

Šī komponente tiek izmantota, lai iegūt lietotāja ievadu (teksta lauks). Šādi tā izskatās:

```kotlin
@Composable
fun EditNumberField(
    value: String,
    onValueChange: (String) -> Unit,
    modifier: Modifier = Modifier
) {

    TextField(
        // Izsauc, veic rekompozīciju, kad mainās vērtība
        value = value,
        // Izsauc nodoto funkciju, kad lietotājs maina ievadi
        onValueChange = onValueChange,
        // Teksta paziņojums lietotājam
        label = { Text(stringResource(R.string.bill_amount)) },
        // Vienas rindas teksta lauks
        singleLine = true,
        // Klaviatūras paramters - tikai ciparu ievads
        keyboardOptions = KeyboardOptions(keyboardType = KeyboardType.Number),
        modifier = modifier

    )
}
```

Šī komponente pieņem 3 lietas:

- `value` - vētība, sagaida mainīgo;
- `onValueChanged` - kad lietotājs ievada datus, tiek izsaukta nodota funkcija;
- `label` - šeit var nodot teksta paziņojumu.

Ir vēl arī papildus parametri:

- `singleLine = true` - iestata teksta laukam tikai 1 teksta rindu;
- `keyboardOptions` - caur šo parametru var iestatīt klaviatūru, šeit atļauj ievadīt tikai skaitļus.

## `EditNumberField` funkcijas analīze

Konkrēti jāpievērš uzmanība šim koda fragmentam:

```kotlin
@Composable
fun EditNumberField(
    value: String,
    onValueChange: (String) -> Unit,
    modifier: Modifier = Modifier
) {
```

Šī funkcija pieņem 3 parametrus:

- `value: String` - šeit sagaida `String` tipa mainīgo;
- `onValueChange: (String) -> Unit` - šeit sagaida `lambda` tipa funkciju. Šī funkcija kā parametru pieņem `String` tipa mainīgo un neko neatgriež, jo `Unit`. Šī funkcija tiek izsaukta, kad lietotājs maina ievadi `TextField`.

## `TipTimeLayout` funkcijas analīze

Konkrēti jāpievērš uzmanība šiem koda fragmentiem:

```kotlin
fun TipTimeLayout() {  
    // Mainīgais, kas saglabā savu vērtību ārpus rekompozīcijas  
    var amountInput by remember { mutableStateOf("") }  
    // Mainīgais, kas glabā ievada datus, konvertē no String uz Double  
    // Operators ?: atgriež 0.0, ja string ir tukšs    
    val amount = amountInput.toDoubleOrNull() ?: 0.0  
    // Mainīgais, kas apstrādā rezultātu  
    val tip = calculateTip(amount)
    
    //...
    
    EditNumberField(  
    // Nododam mainīgo, kas saglabā datus ārpus rekompozīcijas  
    value = amountInput,  
    // Izsauc nodoto funkciju, kad lietotājs maina ievadi (atjauno amountInput)  
    onValueChange = { amountInput = it },  
    modifier = Modifier  
        .padding(bottom = 32.dp)  
        .fillMaxWidth()  
)
```

Darbības princips ir šāds:

1. Lietotājs ievada datus teksta laukā. Teksta lauks izsauc nodoto `lambda` funkciju un ieraksta datus no teksta lauka mainīgā `amountInput`.
2. Notiek rekompozīcija, izvelk datus no mainīgā, konvertē tos uz `double` un veic skaitļošanu, rezultātu izvada uz `Text` elementu.

`value` šeit nepieciešams, lai `TextField` attēlotu lietotāja ievadu un lai `Compose` varētu to atjaunot, kad mainās stāvoklis

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[random metode]]
Nākama lapa >>> [[Switcher]]

---