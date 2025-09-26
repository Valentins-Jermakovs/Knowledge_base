___

**Datums:** 2025-08-09
**Laiks:** 13:24
❚ **Tagi:** #css
⌬ **Priekšmets:**  `CSS`

---
### ⬢ Detalizēts apraksts
#### Par `Box Shadow`

CSS `box-shadow` īpašība tiek izmantota =, lai piešķirt vienu vai vairākas ēnas objektam.

##### Horizontala un vertikāla ēna

![[Pasted image 20250809132633.png]]

```css
div {
  box-shadow: 10px 10px;
}
```

Pirmais parametrs atbilst par horizontāli, otrais par vertikāli. Ēnas krāsu šajā piemērā nosaka teksta krāsa.

##### Krāsas iestatīšana ēnai

![[Pasted image 20250809132751.png]]

```css
div {
  box-shadow: 10px 10px lightblue;
}
```

##### Blur effect pievienošana

![[Pasted image 20250809132835.png]]

```css
div {
  box-shadow: 10px 10px 5px lightblue;
}
```

Par šo efektu atbilst trešais parametrs.

##### Ēnas izplatības rādiusa iestatīšana

![[Pasted image 20250809133021.png]]

```css
div {
  box-shadow: 10px 10px 5px 12px lightblue;
}
```

Par to atbilst ceturtais parametrs.

##### inset parametra iestatīša

![[Pasted image 20250809133147.png]]

```css
div {
  box-shadow: 10px 10px 5px lightblue inset;
}
```

Par to atbilst atslēgas vārds `inset`.

##### Vairāku ēnu uzlikšana

![[Pasted image 20250809133352.png]]

```css
box-shadow: 5px 5px blue, 10px 10px red, 15px 15px green;
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Par text-shadow]]
Nākama lapa >>> [[Pseidoklase hover]]

---
### ⇄ Saistības

Avots >>> [CSS Box Shadow](https://www.w3schools.com/css/css3_shadows_box.asp)
Iepriekšēja lapa >>> [[Navigācija - HTML un CSS]]
Nākama lapa >>> [[Pseidoklase hover]]

---