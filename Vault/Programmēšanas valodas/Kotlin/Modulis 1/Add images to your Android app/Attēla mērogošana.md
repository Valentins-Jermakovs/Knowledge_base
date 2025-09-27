___

**Datums:** 2025-09-21
**Laiks:** 19:01
❚ **Tagi:** #kotlin 

---
# Attēla mērogošana

`ContentScale` nosaka, kā attēls tiek mērogots, lai aizpildītu pieejamo laukumu.

**Piemērs: ContentScale.Crop**

Attēls tiek mērogots, saglabājot proporcijas. Platums un augstums ir vienādi vai lielāki par ekrāna dimensijām → pilnekrāna efekts. Daļa attēla var tikt “nogriezta”, ja tas nesakrīt tieši ar ekrāna proporcijām.

Pielietojuma piemērs:

```kotlin
Image(
    painter = image,
    contentDescription = null,
    contentScale = ContentScale.Crop
)
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Box izmantošana]]
Nākama lapa >>> [[Caurspīdības iestatīšana]]

---