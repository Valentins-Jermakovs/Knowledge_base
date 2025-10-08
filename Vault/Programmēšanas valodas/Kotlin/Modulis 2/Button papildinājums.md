___

**Datums:** 2025-10-08
**Laiks:** 11:55
❚ **Tagi:** #kotlin 

---
# Button papildinājums

Vēl vien piemērs pogu izmantošanai, lai labāk izprast `lambda` funkciju darbību.

`Compose` elementa kods:

```kotlin
@Composable
fun PreviousAndNextButtons(
    modifier: Modifier = Modifier,
    OnPreviuosClick: () -> Unit,
    OnNextClick: () -> Unit,
)
{


    Row (
        verticalAlignment = Alignment.CenterVertically,
        horizontalArrangement = Arrangement.SpaceAround,
        modifier = Modifier
            .fillMaxWidth()
            .padding(5.dp)
    ) {
        Button(onClick = OnPreviuosClick,
            modifier = Modifier
                .width(120.dp)
        )
        {
            Text(text = "Previous")
        }
        Button (onClick = OnNextClick,
            modifier = Modifier
                .width(120.dp)
        )
        {
            Text(text = "Next")
        }
    }
}
```

Šī komponenete atbild par pogu izvietoju un pašām pogām. Tā sagaida 2 `lambda` funkcijas, kas tiek nodotas pogām.

Programmas koda fragments, kur tiek nodotas `lambda` funkcijas pogām:

```kotlin
@Composable
fun ArtSpaceApp(modifier: Modifier = Modifier)
{
    // Mainīgais
    var Screen by remember { mutableStateOf(1) }

    Column (
        verticalArrangement = Arrangement.SpaceAround,
        horizontalAlignment = Alignment.CenterHorizontally,

        modifier = Modifier
            .fillMaxSize()
            .statusBarsPadding()
            .verticalScroll(rememberScrollState())
            .navigationBarsPadding()
    ) {
        ArtworkAndText(Screen = Screen)
        PreviousAndNextButtons(
            OnPreviuosClick = {
                if (Screen > 1)
                {
                    Screen--
                }
                else
                {
                    Screen = 3
                }
            },
            OnNextClick = {
                if (Screen < 3)
                {
                    Screen++
                }
                else
                {
                    Screen = 1
                }
            }
        )
    }
}
```

## Funkciju izmantošana ārpus `Compose`

Šeit tiek parādīts, kā var ārpusē izveidot funkciju un tad to izmantot pogās.

Pašas funkcijas, kas aprakstītas ārpus `Compose` elementa:

```kotlin
fun previousScreen(current: Int, total: Int = 3): Int {
    if (current > 1) {
        return current - 1
    } else {
        return total
    }
}


fun nextScreen(current: Int, total: Int = 3): Int
{
    if (current < total)
    {
	    return current + 1
    }  
    else 
    {
	    return 1
    }
}
```

Šo funkciju pielietojums pogās:

```kotlin
@Composable
fun ArtSpaceApp() {
    var screen by remember { mutableStateOf(1) }
	/*
		Šeit mēs vienalga veidojam lambda tipa funkciju,
		jo button elementi sagaida tieši šo tipu.
		Sākumā veidojam mainīgos, kuri darboja kā lambda.
		Tiem nododam funkciju un mainīgo, kas tiks pārrakstīts.
	*/
    val onPreviousClick = { screen = previousScreen(screen) }
    val onNextClick = { screen = nextScreen(screen) }

    Column {
        ArtworkAndText(Screen = screen)
        PreviousAndNextButtons(
        // Un tad pieslēdzam šīs funkcijas pie pogām
            OnPreviuosClick = onPreviousClick,
            OnNextClick = onNextClick
        )
    }
}

```


> [!NOTE] Atceries!
> Pogas , `Button(onClick = ...)`, sagaida **funkciju bez argumentiem un atgriežamās vērtības**, t.i. `() -> Unit`.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Klaviatūras pogu iestatījumi]]
Nākama lapa >>> [[Programmēšanas valodas/Kotlin/Modulis 2/Navigācija - Modulis 2|Navigācija - Modulis 2]]

---