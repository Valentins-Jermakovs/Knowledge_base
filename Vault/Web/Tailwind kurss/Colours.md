___

**Datums:** 2025-08-11
**Laiks:** 18:00
❚ **Tagi:** #css #tailwind 
⌬ **Priekšmets:**  `Tailwind`

---
### ⬢ Detalizēts apraksts
#### Krāsas

Sintakses piemēri

```
class='bg-{color}-{shade}'
class='text-{color}-{shade}'
class='[bg/text]-[black/white]'
```

Kur:

- `color` - krāsas nosaukums, pieejamas krāsas var apskatīt oficiālā dokumentācijā;\
- `shade` - intensitāte.

`Tailwind` piedāvā krāsas intensitātei šādas vērtības:

- 50, 100, 200, 300, 400, 500, 600
- 700, 800, 900, 950

`class='[bg/text]-[black/white]'` - šāda sintakse tiek izmantota, lai uzlikt balto vai melno krāsu, jo tām nevar piešķirt intensitāti.

```html
<div class='bg-amber-50'></div>
<p class='text-blue-200'>...Some text...</p>
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Element sizing]]
Nākama lapa >>> [[Padding and Margin]]

---