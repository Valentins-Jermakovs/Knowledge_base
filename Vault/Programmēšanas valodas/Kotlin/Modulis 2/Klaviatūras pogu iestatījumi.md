___

**Datums:** 2025-10-08
**Laiks:** 11:18
❚ **Tagi:** #kotlin 

---
# Klaviatūras pogu iestatījumi

Priekš ievada laukiem mērs varam iestatīt tastatūras `action` pogu, kuru nospiežot lietotājs var tikt pārvietots uz nākamo ievades lauku, nosūtīt datus vai pārvietots uz meklēšanas joslu.

```kotlin
EditNumberField(
            label = R.string.bill_amount,
            // Nododam mainīgo, kas saglabā datus ārpus rekompozīcijas
            value = amountInput,
            // Izsauc nodoto funkciju, kad lietotājs maina ievadi (atjauno amountInput)
            onValueChange = { amountInput = it },
            keyboardOptions = KeyboardOptions.Default.copy(
                keyboardType = KeyboardType.Number,
                imeAction = ImeAction.Next
            ),
            modifier = Modifier
                .padding(bottom = 32.dp)
                .fillMaxWidth()
        )
        EditNumberField(
            label = R.string.how_was_the_service,
            value = tipInput,
            onValueChange = { tipInput = it},
            keyboardOptions = KeyboardOptions.Default.copy(
                keyboardType = KeyboardType.Number,
                imeAction = ImeAction.Done
            ),
            modifier = Modifier.padding(bottom = 32.dp).fillMaxWidth()
        )
```

Jāpievērš uzmanību šim te koda fragmentam:

```kotlin
keyboardOptions = KeyboardOptions.Default.copy(
                keyboardType = KeyboardType.Number,
                imeAction = ImeAction.Next
            )
```

Pirmā koda rinda ir standarta priekš visa, atšķirības sākas otrā koda rindā:

- `KeyboardType.klaviatūrasTips` - šeit tu norādi kādu klaviatūras tipu iestatīt;
- `imeAction.veids` - šeit tu norādi `action` pogas veidu.

Populārākie `imeAction`:

- `Search` - tiek izmantots, kad mekllētājs grib veikt meklēšanu;
- `Send` - tiek izmantots, kad lietotājs grib nosūtīt tekstu no teksta ievades lauka, analogs `submit` pogai.
- `Go` - tiek izmantots, ja lietotājs vēlas pāriet uz ievades teksta mērķi.
- `Next` - tiek izmantots, lai pārvietot lietotāju uz nākamo ievades lauku.

**Klaviatūru veidi**

| Tips                          | Apraksts                                                               |
| ----------------------------- | ---------------------------------------------------------------------- |
| `KeyboardType.Text`           | Parasta teksta tastatūra (pēc noklusējuma).                            |
| `KeyboardType.Ascii`          | Tikai ASCII rakstzīmes (latīņu burti, cipari, pieturzīmes).            |
| `KeyboardType.Number`         | Tikai cipari (0–9).                                                    |
| `KeyboardType.NumberPassword` | Ciparu ievade ar simbolu maskēšanu (piemēram, PIN kodiem vai parolēm). |
| `KeyboardType.Phone`          | Tastatūra telefona numuram (ietver +, #, * un ciparus).                |
| `KeyboardType.Uri`            | Tastatūra URL ievadei (ietver "/", ".", u.c.).                         |
| `KeyboardType.Email`          | Tastatūra e-pasta adresei (ietver "@", ".").                           |
| `KeyboardType.Password`       | Tastatūra parolēm ar simbolu maskēšanu.                                |
| `KeyboardType.Decimal`        | Ciparu tastatūra ar decimālo punktu (cipari + punkts).                 |

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[ScrollVertical]]
Nākama lapa >>> [[Button papildinājums]]

---