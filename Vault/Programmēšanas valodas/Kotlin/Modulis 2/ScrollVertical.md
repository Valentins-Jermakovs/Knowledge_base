___

**Datums:** 2025-10-08
**Laiks:** 11:18
❚ **Tagi:** #kotlin 

---
# ScrollVertical

Atribūts `VerticalScroll` ļauj padarīt programmu adoptīvu, skrollējamu:

```kotlin
Column(
        modifier = Modifier
            .statusBarsPadding()
            .padding(40.dp)
            // Pievieno skrollu
            .verticalScroll(rememberScrollState()),
```

To vajag iestatīt konteinerim, izmantojot `modifier`. Tad programma būs skrollējama. Īpaši noder, kad ekrāns ir horizontālā skatā.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Switcher]]
Nākama lapa >>> [[Klaviatūras pogu iestatījumi]]

---