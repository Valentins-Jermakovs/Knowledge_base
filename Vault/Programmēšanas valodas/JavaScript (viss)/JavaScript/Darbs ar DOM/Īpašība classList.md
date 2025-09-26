___

**Datums:** 2025-08-17
**Laiks:** 15:42
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Īpašība `classList`

Šī īpašība tiek izmantota, lai pārvaldīt klases `html` elementiem, tā satur 3 metodes:

- `add(className)` - pievieno klasi `className`;
- `remove(className)` - izdzēš klasi `className`;
- `toggle(className)` - pārslēdz elementa klasi uz className. Ja klases nav, tā tiek pievienota, ja tāda ir, tā tiek noņemta.

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
    <style>
        .header-color {color:navy;}
        .header-font {font-family: Verdana;}
        .header-size {font-size: 22px;}
    </style>
</head>
<body>
    <h1 id="header" class="header-size">Home Page</h1>
    <script>
    const header = document.getElementById("header");
    header.classList.remove("header-size");     //  удаляем класс header-size
    header.classList.add("header-font");        // добавляем класс header-font
    header.classList.toggle("header-color");    // переключаем класс header-color
    </script>
</body>
</html>
```

##### Metode `toggle`

*Piezīme. Šī metode var pieņem otro parametru (neobligāts), ja vērtība `true`, klase tiek pārslegta.*

```js
const i = 5;
const condition = i > 0; // условие
const header = document.getElementById("header");
header.classList.toggle("header-color", condition);    // переключаем класс header-color по условию
```

##### Papildus informācija

Nepieciešamības pēc mēs varam iterēt pa klasēm, vai iegūt mums nepieciešamo pēc indeksa:

```js
// перебор списка классов
for(headerClass of header.classList){
    console.log(headerClass);
}
console.log(header.classList[0]);   // первый установленный класс
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Управление стилем и классами элементов](https://metanit.com/web/javascript/8.7.php)
Iepriekšēja lapa >>> [[Navigācija JavaScript]]

---