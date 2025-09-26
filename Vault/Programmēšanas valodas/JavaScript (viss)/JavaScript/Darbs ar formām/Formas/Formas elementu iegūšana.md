___

**Datums:** 2025-08-25
**Laiks:** 11:21
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Formas elementu iegūšana

##### Metodes

Standarta metodes, lai iegūt formas elementu:

- `getElementById()` - pēc `id`
- `getElementsByClassName()` - pēc klases nosaukuma
- `getElementsByTagName()` - pēc taga
- `getElementsByName()` - pēc `name`
- `querySelector()` - pēc selektora
- `querySelectorAll()` - pēc selektora

```js
// получаем элемент по id="key"
const keyField = document.getElementById("key");
console.log(keyField);
```

##### `elements` īpašība

šādi var iegūt formas elementus, izmantojot `elements`:

```js
const form = document.getElementById("search");
// получение поля по индексу
const keyField = form.elements[0];
console.log(keyField);
// получение этого же поля, но через имя
const keyField2 = form.elements["q"];
console.log(keyField2);
```

##### Pēc `name`

Izmantojot formas un elementa `name`:

```js
// поле q на форме search
const keyField = document.search.q;
console.log(keyField);
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Формы и их элементы](https://metanit.com/web/javascript/10.1.php)
Iepriekšēja lapa >>> [[Formu īpašības un metodes]]
Nākama lapa >>> [[Formas elementu īpašības]]

---