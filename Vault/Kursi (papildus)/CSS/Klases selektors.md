___

**Datums:** 2025-08-08
**Laiks:** 18:34
❚ **Tagi:** #css 
⌬ **Priekšmets:**  `CSS`

---
### ⬢ Detalizēts apraksts
#### Par klases selektoru

Salidzinājuma ar `elementu` selektoriem, kas darbojas uz visiem vienāda tipa elementiem.
*Tas nozīmē, piem., `img` vai `p`, stili darbosies uz visiem šāda tipa elementiem.*

`CSS` ļauj izmantot arī pašu definētas klases.

```html
<p class='message'>Hello!</p>
<p>Good by!</p>
```

```css
.message {
	color: red;
}
```

Klases selektors sākas ar `.` punktu un stils darbosies tikai uz tiem elementiem, pret kuriem ir attiecināma šī klase. Tas nozīmē, kā var eksistēt vairāki elementi ar vienu un to pašu klasi.

> Vienam elementam var piešķirt arī vairākas klases. Klases savā starpā atdala ar `space`.

```html
<p class='text italic'>Some text...</p>
```

##### Utility class

Tas ir tādas klases, kas tiek izmantotas uz vairākiem objektiem un tās atbild var vienu konkrētu lietu, piemēram, piešķirt tekstam stilu `italic`.

```css
.italic {
	font-style: italic;
}
```

Ja vajag tikai vienu kādu eksemplāru, unikālu, tad izmanto `id` unikālo identifikātoru.

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Navigācija - HTML un CSS (2. daļa) strukturēts saturs]]
Nākama lapa >>> [[Grupas selektors]]

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[alt atribūts]]
Nākama lapa >>> [[justify content]]

---