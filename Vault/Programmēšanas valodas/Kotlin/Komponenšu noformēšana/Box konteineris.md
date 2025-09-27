___

**Datums:** 2025-09-27
**Laiks:** 18:51
❚ **Tagi:** #kotlin 

---
# Box konteineris


> [!NOTE] Box konteineris
> Tas ir viens no pamatelementiem **konteineriem**, kas ļauj sakraut citus elementus vienu uz otra.

**Box** ir kā “kaste”, kurā vari likt citus Compose elementus.
Visi bērnelementi tiek **novietoti viens uz otra**, un tos var līdzināt ar **alignment**.    
Ļoti noder, ja gribi, piemēram, **fonu ar tekstu virs tā** vai **attēlu ar ikonām virs**.

```kotlin
Box(
    modifier = Modifier
        .size(200.dp)
        .background(Color.LightGray),
    contentAlignment = Alignment.Center // kā bērnelementi tiks centrēti
) {
    Text("Teksts Box iekšpusē", color = Color.Black)
    Image(
        painter = painterResource(R.drawable.my_image),
        contentDescription = "Attēls Box iekšpusē",
        modifier = Modifier.size(100.dp)
    )
}
```

**Box galvenās īpašības**

| Parametrs / funkcija      | Ko dara                                                               |
| ------------------------- | --------------------------------------------------------------------- |
| `modifier`                | Kontrolē Box izmēru, fonu, apmali, padding utt.                       |
| `contentAlignment`        | Līdzinājums visiem bērnelementiem (`TopStart`, `Center`, `BottomEnd`) |
| `propagateMinConstraints` | Ja `true`, bērni var pārsniegt Box minimālos izmērus                  |
| `content`                 | Visi bērnelementi Box iekšpusē, var būt Text, Image, Row, Column utt. |

## 🔗 Kā strādā Box

- Bērni tiek **sakrauti vienu uz otra**, ja nevienam nav alignment → visi augšējā kreisajā stūrī.
- `contentAlignment` ļauj visiem bērniem dot **noklusējuma līdzinājumu**.
- Katram bērnam var vēl pielikt **savu Modifier**, lai novietotu citur vai mainītu izmēru.

```kotlin
Box(modifier = Modifier.size(200.dp), contentAlignment = Alignment.Center) {
    Text("Centrā")
    Text("Augšā pa kreisi", modifier = Modifier.align(Alignment.TopStart))
}
```

Šajā piemērā viens teksts būs centrā, otrs – augšējā kreisajā stūrī, jo mēs lietojām `align()` uz bērna.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Modifier]]
Nākama lapa >>> [[Column konteineris]]

---