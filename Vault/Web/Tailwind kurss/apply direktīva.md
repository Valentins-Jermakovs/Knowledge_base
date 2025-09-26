___

**Datums:** 2025-08-12
**Laiks:** 16:16
❚ **Tagi:** #css #tailwind 
⌬ **Priekšmets:**  `Tailwind`

---
### ⬢ Detalizēts apraksts
#### `@apply` direktīva

Ja parasti `tailwind` klases izmanto pašā `htlm` dokumentā, var izmantot arī `tailwind` klases `styles.css` failā. Tu veido klasi un tajā izmanto `tailwind` klases. Tas ekonomēs vietu `html` dokumetā un padarīs kodu pārskatamāku.

```css
@tailwind base;
@tailwind components;
@tailwind utilities;

.card {
	@apply bg-white rounded relative
}
```

Tādējādi var veidot gatavu dizainu elementiem.

Ar tīro `html` nedarbojas!!!

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Web/Tailwind kurss/Pozicionēšana|Pozicionēšana]]
Nākama lapa >>> [[Grid izkārtojums]]

---