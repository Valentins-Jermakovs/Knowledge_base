___

**Datums:** 2025-08-11
**Laiks:** 14:16
❚ **Tagi:** #css #flexbox 
⌬ **Priekšmets:**  `Flexbox`

---
### ⬢ Detalizēts apraksts
#### `align-self` īpašība

Šī īpašība tiek izmantota pret kādu konkrētu elementu `flex` konteinerī.

```
align-self: auto|stretch|center|flex-start|flex-end|baseline|;
```

| Vērtība      | Apraksts                                                                                                                          |
| ------------ | --------------------------------------------------------------------------------------------------------------------------------- |
| `auto`       | Noklusējuma vērtība. Elements pārmanto vecākelementa `align-items` īpašību vai tiek iestatīts uz “stretch”, ja vecākelements nav. |
| `stretch`    | Elements tiek izstiepts, lai aizpildītu konteineru.                                                                               |
| `center`     | Elements tiek novietots konteinera centrā.                                                                                        |
| `flex-start` | Elements tiek novietots konteinera sākumā.                                                                                        |
| `flex-end`   | Elements tiek novietots konteinera beigās.                                                                                        |
| `baseline`   | Elements tiek novietots konteinera pamatlīnijā.                                                                                   |

```css
#myBlueDiv {
  align-self: center;
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Selektors >]]
Nākama lapa >>> [[Par flex]]

---