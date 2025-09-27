___

**Datums:** 2025-09-21
**Laiks:** 18:53
❚ **Tagi:** #kotlin 

---
# Box izmantošana

**Box** ir viens no trīs pamata layout elementiem (Column, Row, Box). Tas ļauj pārklāt elementus vienu virs otra (piem., bilde fonā, teksts priekšplānā).  Var noteikt izkārtojuma pozīciju elementiem, kas atrodas Box iekšpusē.

```kotlin
@Composable
fun GreetingImage(message: String, from: String, modifier: Modifier = Modifier) {
    val image = painterResource(R.drawable.androidparty)
    Box(modifier) {
        Image(
            painter = image,
            contentDescription = null
        )
        GreetingText(
            message = message,
            from = from,
            modifier = Modifier
                .fillMaxSize()
                .padding(8.dp)
        )
    }
}
```

Šeit teksts tiks izvietots virs attēla, jo tiek pielietots Box tipa konteineris.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Attēla attēlošana uz ekrāna]]
Nākama lapa >>> [[Attēla mērogošana]]

---