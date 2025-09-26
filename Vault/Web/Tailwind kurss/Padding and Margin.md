___

**Datums:** 2025-08-11
**Laiks:** 18:24
❚ **Tagi:** #css #flexbox 
⌬ **Priekšmets:**  `Flexbox`

---
### ⬢ Detalizēts apraksts
#### Padding and Margin

##### Sintakse malu iestatīšanai

Sintakse

```
Visu 4 pušu iestatīšana:

class='p-{value}'
class='m-{value}'
```

> Remember, 1 unit = 0.25 rem = 4px

Lai iestatītu kādu konkrētu pusi, izmanto šādu sintaksi:

```
class='[p/m]{side}-{value}'
```

| Side | Meaning |
| ---- | ------- |
| `t`  | top     |
| `b`  | bottom  |
| `l`  | left    |
| `r`  | right   |
Lai iestatīt 2 puses pa reizi, horizontāli vai vertikāli, izmanto šādus *side*:

| Side | Meaning    |
| ---- | ---------- |
| `x`  | left&right |
| `y`  | top&bottom |
##### Sintakse centrēšanai

Sintakse:

```
class='m{side}-value'
```

Šī lieta tiek izmantota `block` tipa elementiem, piem., `<div>` konteineriem, lai tos centrēt.

| Side      | Meaning                                     |
| --------- | ------------------------------------------- |
| `m-auto`  | `margin:auto;`                              |
| `mx-auto` | `margin-left:auto;`<br>`margin-right:auto`; |
| `my-auto` | `margin-top:auto;`<br>`margin-bottom:auto;` |

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Colours]]
Nākama lapa >>> [[Fonti]]

---