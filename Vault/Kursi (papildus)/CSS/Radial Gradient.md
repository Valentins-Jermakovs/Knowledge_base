___

**Datums:** 2025-08-10
**Laiks:** 15:19
❚ **Tagi:** #css
⌬ **Priekšmets:**  `CSS`

---
### ⬢ Detalizēts apraksts
#### Radial Gradient

![[Pasted image 20250810152056.png]]

`Radial gradient` ir krāsu pāreja, kas definējas ap savu centru un izplatās visos virzienos no centra.

**Sintakse**

```css
background-image: radial-gradient(shape size at position, start-color, ..., last-color);
```

- **shape** - forma, var būt `ellipse` (noklusējums) vai `circle`;
- **size** - izmērs, var būt `closest-side`, `farthest-side`, `closest-corner` vai `farthest-corner` (noklusējums);
- **position** - centra pozīcija, noklusējuma vērtība ir `center`;
- **color stops** - vismaz divas krāsas, kas definē pāreju.

##### Piemēri

**Vienmērīgi izvietoti krāsu punkti (noklusējums)**

```css
#grad {
  background-image: radial-gradient(red, yellow, green);
}
```

Krāsas tiek vienmērīgi izkliedētas no centra uz malu.

**Atšķirīgi izvietoti krāsu punkti**

```css
#grad {
  background-image: radial-gradient(red 5%, yellow 15%, green 60%);
}
```

Katram krāsu punktam var norādīt precīzu attālumu no centra (%).

##### Gradienta formas

| Vērtība (shape) | Skaidrojums                                   | Noklusējums |
| --------------- | --------------------------------------------- | ----------- |
| `ellipse`       | Elipse (garuma un platuma ass var atšķirties) | ✔           |
| `circle`        | Aplis                                         | ✖           |

```css
background-image: radial-gradient(circle, red, yellow, green);
```

##### Gradienta izmēri

|Vērtība (size)|Skaidrojums|
|---|---|
|`closest-side`|Līdz tuvākajai konteinerā esošajai malai|
|`farthest-side`|Līdz tālākajai konteinerā esošajai malai|
|`closest-corner`|Līdz tuvākajam konteinerā esošajam stūrim|
|`farthest-corner`|Līdz tālākajam konteinerā esošajam stūrim (noklusējums)|

```css
background-image: radial-gradient(closest-side at 60% 55%, red, yellow, black);
```

##### Atkārtots radiālais gradients

Funkcija `repeating-radial-gradient()` ļauj radīt atkārtotus radiālos gradientus.

```css
#grad {
  background-image: repeating-radial-gradient(red, yellow 10%, green 15%);
}
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Linear Gradient]]
Nākama lapa >>> [[Conic Gradient]]

---
### ⇄ Saistības

Avots >>> [CSS Radial Gradients](https://www.w3schools.com/css/css3_gradients_radial.asp)
Iepriekšēja lapa >>> [[Linear Gradient]]
Nākama lapa >>> [[Conic Gradient]]

---