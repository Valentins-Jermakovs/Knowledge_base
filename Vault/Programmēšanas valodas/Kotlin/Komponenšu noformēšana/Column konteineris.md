___

**Datums:** 2025-09-27
**Laiks:** 18:53
❚ **Tagi:** #kotlin 

---
# Column konteineris


> [!NOTE] Column
> **Column** kārto bērnelementus **vertikāli** (no augšas uz leju).

Līdzīgi kā HTML `<div> ar flex-direction: column`.
Noder, ja gribi sakārtot vairākus elementus vertikālā secībā: tekstu virs attēla, pogas zem teksta utt.

```kotlin
Column(
    modifier = Modifier
        .fillMaxWidth()
        .background(Color.LightGray)
        .padding(16.dp),
    verticalArrangement = Arrangement.spacedBy(8.dp), // attālums starp bērniem
    horizontalAlignment = Alignment.CenterHorizontally // līdzinājums horizontāli
) {
    Text("Pirmais teksts")
    Image(
        painter = painterResource(R.drawable.my_image),
        contentDescription = "Attēls Column iekšpusē",
        modifier = Modifier.size(100.dp)
    )
    Text("Otrais teksts")
}
```


**Column galvenās īpašības**

| Parametrs / funkcija      | Ko dara                                                                     |
| ------------------------- | --------------------------------------------------------------------------- |
| `modifier`                | Kontrolē Column izmēru, fonu, apmali, padding utt.                          |
| `verticalArrangement`     | Kā bērni tiks izkārtoti vertikāli (`Top`, `Center`, `Bottom`, `spacedBy()`) |
| `horizontalAlignment`     | Kā bērni tiks līdzināti horizontāli (`Start`, `CenterHorizontally`, `End`)  |
| `propagateMinConstraints` | Ja `true`, bērni var pārsniegt Column minimālos izmērus                     |
| `content`                 | Bērnelementi Column iekšpusē, var būt Text, Image, Row, Box utt.            |

## 🔗 Kā strādā Column

- Bērni tiek **kārtoti vertikāli**, viens zem otra.
- `verticalArrangement` kontrolē **attālumu starp bērniem** vai to izvietojumu.
- `horizontalAlignment` kontrolē **līdzinājumu pa X asi** visiem bērniem.
- Katram bērnam var pielikt **Modifier**, lai mainītu izmēru vai novietojumu individuāli.

```kotlin
Column(
    modifier = Modifier.fillMaxWidth(),
    verticalArrangement = Arrangement.SpaceBetween,
    horizontalAlignment = Alignment.Start
) {
    Text("Augšā")
    Text("Vidū", modifier = Modifier.align(Alignment.CenterHorizontally))
    Text("Apakšā")
}
```

Šeit Column sadala vietu starp augšu un leju, bet konkrētam bērnam var uzlikt citu align.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Box konteineris]]
Nākama lapa >>> [[Row konteineris]]

---