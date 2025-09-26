___

**Datums:** 2025-08-17
**Laiks:** 15:25
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Atribūta iegūšana

Lai iegūt elementa/mezgla atribūtu, tiek izmantota metode `getAttribute()`, kas atgriež norādīta atribūta vērtību:

```html
<a id="home" class="link" href="index.html">Home</a>
```

```js
// получаем элемент
const element = document.getElementById("home");
// получаем атрибуты элемента
console.log(element.getAttribute("id"));    // home
console.log(element.getAttribute("class")); // link
console.log(element.getAttribute("href"));  // index.html
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Управление атрибутами элементов](https://metanit.com/web/javascript/8.9.php)
Iepriekšēja lapa >>> [[Atribūtu pārvaldības metodes]]
Nākama lapa >>> [[Atribūtu iestatīšana]]

---