___

**Datums:** 2025-08-10
**Laiks:** 15:22
❚ **Tagi:** #css
⌬ **Priekšmets:**  `CSS`

---
### ⬢ Detalizēts apraksts
#### Par Conic Gradients

`Conic gradient` ir krāsu pāreja, kas rotē ap centrālo punktu, veidojot kūkas šķēles (konusveida) efektu.

Sintakse

```css
background-image: conic-gradient([from angle] [at position,] color [degree], color [degree], ...);
```

- **from angle** — rotācijas sākuma leņķis (noklusējums `0deg`);
- **at position** — centra pozīcija (noklusējums `center`);
- **color [degree]** — krāsa ar opciju norādīt leņķi, kurā tā beidzas;
- Vismaz divas krāsas ir jānorāda.

Ja leņķi nav norādīti, krāsas tiek vienmērīgi sadalītas ap centru.

##### Piemēri

**Piemērs ar trim krāsām**

![[Pasted image 20250810152836.png]]

```css
#grad {
  background-image: conic-gradient(red, yellow, green);
}
```

**Piemērs ar trim krāsām un to leņķiem**

![[Pasted image 20250810152852.png]]

```css
#grad {
  background-image: conic-gradient(red 45deg, yellow 90deg, green 210deg);
}
```

**Kūkas diagramma**

![[Pasted image 20250810152907.png]]

Lai konusa gradients izskatītos kā kūkas diagramma, pievieno `border-radius: 50%;`

```css
#grad {
  background-image: conic-gradient(red, yellow, green, blue, black);
  border-radius: 50%;
}
```

**Ar noteiktiem leņķiem:**

![[Pasted image 20250810153007.png]]

```css
#grad {  background-image: conic-gradient(red 0deg, red 90deg, yellow 90deg, yellow 180deg, green 180deg, green 270deg, blue 270deg);  
  border-radius: 50%;}
```

**Konusa gradienta rotācija - `from angle`**

![[Pasted image 20250810152921.png]]

Ar `from` var norādīt, no kura leņķa sākt rotāciju.

```css
#grad {
  background-image: conic-gradient(from 90deg, red, yellow, green);
}
```

**Konusa gradienta centra pozīcija — `at position`**

![[Pasted image 20250810153134.png]]

```css
#grad {  background-image: conic-gradient(at 60% 45%, red, yellow, green);}
```

**Atkārtots konusa gradients**

Funkcija `repeating-conic-gradient()` ļauj gradientu atkārtot.

![[Pasted image 20250810153255.png]]

```css
#grad {
  background-image: repeating-conic-gradient(red 10%, yellow 20%);
  border-radius: 50%;
}
```

![[Pasted image 20250810153306.png]]

```css
#grad {
  background-image: repeating-conic-gradient(
    red 0deg 10deg,
    yellow 10deg 20deg,
    blue 20deg 30deg
  );
  border-radius: 50%;
}
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Radial Gradient]]
Nākama lapa >>> [[Navigācija - HTML un CSS (2. daļa) strukturēts saturs]]

---
### ⇄ Saistības

Avots >>> [CSS Conic Gradients](https://www.w3schools.com/css/css3_gradients_conic.asp)
Iepriekšēja lapa >>> [[Radial Gradient]]
Nākama lapa >>> [[em tags]]

---