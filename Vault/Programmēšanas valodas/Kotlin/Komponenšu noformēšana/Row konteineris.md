___

**Datums:** 2025-09-27
**Laiks:** 18:59
❚ **Tagi:** #kotlin 

---
# Row konteineris


> [!NOTE] Row
> Row kārto bērnelementus horizontāli (no kreisās uz labo).

Līdzīgi kā HTML `<div>` ar `flex-direction: row`.
Noder, ja gribi izvietot vairākus elementus **blakus**: pogas, ikonas, tekstu rindā utt.

```kotlin
Row(
    modifier = Modifier
        .fillMaxWidth()
        .background(Color.LightGray)
        .padding(16.dp),
    horizontalArrangement = Arrangement.spacedBy(8.dp), // attālums starp bērniem
    verticalAlignment = Alignment.CenterVertically // līdzinājums vertikāli
) {
    Text("Poga 1")
    Text("Poga 2")
    Image(
        painter = painterResource(R.drawable.my_image),
        contentDescription = "Attēls Row iekšpusē",
        modifier = Modifier.size(50.dp)
    )
}
```

**Row galvenās īpašības**

| Parametrs / funkcija      | Ko dara                                                                      |
| ------------------------- | ---------------------------------------------------------------------------- |
| `modifier`                | Kontrolē Row izmēru, fonu, apmali, padding utt.                              |
| `horizontalArrangement`   | Kā bērni tiks izkārtoti horizontāli (`Start`, `Center`, `End`, `spacedBy()`) |
| `verticalAlignment`       | Kā bērni tiks līdzināti vertikāli (`Top`, `CenterVertically`, `Bottom`)      |
| `propagateMinConstraints` | Ja `true`, bērni var pārsniegt Row minimālos izmērus                         |
| `content`                 | Bērnelementi Row iekšpusē, var būt Text, Image, Column, Box utt.             |

## 🔗 Kā strādā Row

- Bērni tiek **kārtoti horizontāli**, viens blakus otram.
- `horizontalArrangement` kontrolē **attālumu starp bērniem** vai to izvietojumu.
- `verticalAlignment` kontrolē **līdzinājumu pa Y asi** visiem bērniem.
- Katram bērnam var pielikt **Modifier**, lai mainītu izmēru vai novietojumu individuāli.

```kotlin
Row(
    modifier = Modifier.fillMaxWidth(),
    horizontalArrangement = Arrangement.SpaceBetween,
    verticalAlignment = Alignment.CenterVertically
) {
    Text("Kreisais")
    Text("Centrā", modifier = Modifier.align(Alignment.CenterVertically))
    Text("Labais")
}
```

Šeit Row izvieto bērnus pa visu platumu, bet konkrētam bērnam var uzlikt savu align.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Column konteineris]]
Nākama lapa >>> [[Navigācija - Komponenšu noformēšana]]

---