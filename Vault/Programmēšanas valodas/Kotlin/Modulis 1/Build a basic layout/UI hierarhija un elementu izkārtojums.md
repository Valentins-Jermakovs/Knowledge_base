___

**Datums:** 2025-09-21
**Laiks:** 11:48
❚ **Tagi:** #kotlin 

---
# UI hierarhija un elementu izkārtojums

**Pamatideja**:

- UI balstās uz **iekļaušanu (containment)**.
- **Vecākelements (parent)** var saturēt vienu vai vairākus **bērnelementus (child)**.
- Bērnelementi paši var saturēt citus elementus → veidojas hierarhija.

## Pamatizkārtojuma elementi

Jetpack Compose nodrošina trīs galvenos Composable izkārtojumus:

1. **Column** - Izvieto elementus **vertikāli**, katrs bērnelements atrodas zem iepriekšējā;
2. **Row** - Izvieto elementus **horizontāli**, katrs bērnelements atrodas blakus iepriekšējam;
3. **Box** - Elementi tiek novietoti **viens virs otra** (pārklājoties).

![[Pasted image 20250921115118.png]]

Piemērs ar `Row`:

```kotlin
// Don't copy.
Row {
    Text("First Column")
    Text("Second Column")
}
```

![[Pasted image 20250921115150.png]]

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Fonta izmēra maiņa]]
Nākama lapa >>> [[Teksta elementu izvietošana rindā]]

---