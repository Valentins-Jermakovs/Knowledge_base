___

**Datums:** 2025-09-21
**Laiks:** 19:20
❚ **Tagi:** #kotlin 

---
# Paddingi

**Padding** ir iekšēja atstarpe starp konteineri un tā saturu.

![[2e96e127f9f8c7_1440.png]]

Mēs varam caur `modifier` iestātīt kā katru malu atsevišķi:

```kotlin
// This is an example.
Modifier.padding(
    start = 16.dp,
    top = 16.dp,
    end = 16.dp,
    bottom = 16.dp
)
```

Tā arī visas uzreiz:

```kotlin
modifier = Modifier
    .padding(16.dp)
    .align(alignment = Alignment.End)
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Layout Modifiers]]
Nākama lapa >>> [[Teksta izvietošana resursu failā]]

---