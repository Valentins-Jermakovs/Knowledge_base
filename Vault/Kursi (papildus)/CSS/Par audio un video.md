___

**Datums:** 2025-08-10
**Laiks:** 15:42
❚ **Tagi:** #css 
⌬ **Priekšmets:**  `CSS`

---
### ⬢ Detalizēts apraksts
#### Par audio un video

Šiem tagiem ir specifiski atribūti:

- `controls` - kontroles elementi;
- `muted` - izslēgta skaņa;
- `loop` - ieciklēts;
- `autoplay` - automātiska atskaņošana.

Pastāv arī tāds iekšējs tags `<source>` ar atribūtu `type`.

```html
<audio>
	<source src='ceļš_līdz_failam' type='audio/mp3'>
	<source src='ceļš_līdz_failam' type='audio/wav'>
</audio>
```

Tags `source` ļauj ievietot vienu un to pašu failu dažādos formātos, ja nu pārluks vienu no tiem nevar atskaņot, paņems to, kuru var. Atribūts `type` pasaka pārlūkam par faila formātu.

Tags `<source>` attiecināms arī uz video. 
Video objektam var piešķirt arī izmērus, taču tie tiek skaitīti pikseļos. Izmēri tiek iestatīti `html` dokumentā.

```html
<video width='200' height='100'> </video>
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[strong tags]]
Nākama lapa >>> [[Navigācija - HTML un CSS (2. daļa) strukturēts saturs]]

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[strong tags]]
Nākama lapa >>> [[Grupas selektors]]

---