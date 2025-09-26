___

**Datums:** 2025-08-11
**Laiks:** 14:37
❚ **Tagi:** #css #flexbox 
⌬ **Priekšmets:**  `Flexbox`

---
### ⬢ Detalizēts apraksts
#### `@media`

`@media` izmanto **media queries**, lai pielāgotu stilus dažādiem ekrāna izmēriem, orientācijām vai ierīču īpašībām.  
Tas ir pamats **responsīvam dizainam**.

**Var pārbaudīt:**

- Skata loga (`viewport`) platumu/augstumu;
- Ierīces orientāciju (portrets / ainava);
- Ekrāna izšķirtspēju;
- Ievades ierīces īpašības (pele, skārienekrāns u.c.);
- Izejas ierīces tipu.

**Mediatipi:**

- `all` – visi ierīču tipi (noklusējums);
- `screen` – monitori, planšetes, tālruņi u.c. ekrāni;
- `print` – drukai;
- `speech` – ekrānlasītāji.

**Sintakse:**

```css
@media [not|only] mediatips and (medija_īpašība) {
  CSS-kods;
}
```

**Atslēgvārdi:**

- `not` – apgriež nosacījuma nozīmi
- `only` – ignorē vecos pārlūkus bez media queries atbalsta
- `and` – apvieno vairākus nosacījumus

##### Piemēri

**Piemērs 1 – Mainīt fona krāsu mazākiem ekrāniem**

```css
@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

**Piemērs 2 – Adaptīvs izkārtojums kolonnām**

```css
@media screen and (max-width: 992px) {
  .column { width: 50%; }
}

@media screen and (max-width: 600px) {
  .column { width: 100%; }
}
```

**Piemērs 3 – Visiem ierīču tipiem**

```css
@media all and (min-width: 800px) {
  p {
    font-size: 18px;
    line-height: 1.6;
  }
}
```

---
### ⇄ Saistības

Avots >>> [CSS @media Rule](https://www.w3schools.com/cssref/atrule_media.php)
Iepriekšēja lapa >>> [[Par order]]
Nākama lapa >>> [[Navigācija - Flexbox]]

---