___

**Datums:** 2025-09-27
**Laiks:** 18:37
❚ **Tagi:** #kotlin 

---
# Attēla noformēšana

**Jetpack Compose attēla parametri (Image)**

|Parametrs|Paskaidrojums|
|---|---|
|`painter`|Avots, no kura tiek ņemts attēls (`painterResource`, `rememberImagePainter`)|
|`contentDescription`|Teksts ekrāna lasītājiem (pieejamībai, ja nav vajadzīgs – `null`)|
|`modifier`|Izmēri, novietojums, klikšķi utt. (nav obligāti, bet parasti lieto)|
|`alignment`|Attēla saturs lodziņā (`Center`, `TopStart`, `BottomEnd` utt.)|
|`contentScale`|Kā attēls tiek mērogots (`FillBounds`, `Crop`, `Fit`, `FillHeight`, `Inside`)|
|`alpha`|Caurspīdīgums (no `0f` līdz `1f`)|
|`colorFilter`|Krāsu filtrs (`ColorFilter.tint(Color.Red)`)|
**Koda piemērs ar parametriem tieši Image(...)**

```kotlin
Image(
    painter = painterResource(id = R.drawable.my_image),
    contentDescription = "Demo attēls",
    alignment = Alignment.Center,
    contentScale = ContentScale.Crop,
    alpha = 0.9f,
    colorFilter = ColorFilter.tint(Color.Red)
)
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Teksta noformēšana]]
Nākama lapa >>> [[Modifier]]

---