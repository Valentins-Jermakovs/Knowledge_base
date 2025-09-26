___

**Datums:** 2025-09-21
**Laiks:** 19:08
❚ **Tagi:** #kotlin 

---
# Layout Modifiers

**Modifier** ir veids, kā **dekorēt vai pievienot uzvedību** Compose UI elementiem. **Modifier nosaka “konteineru” īpašības**, nevis pašu saturu.

Ar modifier vari:

- Pievienot **fona krāsu**;
- Noteikt **padding** (atstarpes);
- Mainīt **izmēru, izvietojumu, alfa/transparenci**;
- Pievienot **uzvedību** (klikšķus, ritināšanu utt.).

```kotlin
Text(
    text = "Hello, World!",
    modifier = Modifier.background(color = Color.Green) // fons
)
```

## Modifiers izkārtojuma elementiem

Modifiers var izmantot arī **Row**, **Column** un **Box** elementiem, lai pozicionētu iekšējos bērnus:
    
**Column**:
- `verticalArrangement` – kā sadalīt bērnus vertikāli;
- `horizontalAlignment` – bērnu horizontālā izlīdzināšana (start, center, end).

![[df69881d07b064d0.gif]]

**Row**:
- `horizontalArrangement` – bērnu izvietojums horizontāli;
- `verticalAlignment` – bērnu vertikālā izlīdzināšana (top, center, bottom).

![[c1e6c40e30136af2.gif]]

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Caurspīdības iestatīšana]]
Nākama lapa >>> [[Paddingi]]

---