___

**Datums:** 2025-08-25
**Laiks:** 11:28
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Formas elementu īpašības

Formas elementiem ir šādas īpašības:

- `name` - ļauj iegūt nosaukumu;
- `value` - iegūt, mainīt saturu;
- `type` - nolasīt tipu;

```html
<form name="search">
    <input type="text" name="key" value="hello world"></input>
    <input type="submit" name="send"></input>
</form>
<script>
const form = document.getElementById("search");
// получение поля формы по имени
const keyField = form.elements["key"];
// получение значения поля
console.log(keyField.value);
// установка значения поля
keyField.value = "Enter a string";
</script>
```

```js
const form = document.getElementById("search");
// получение поля формы по имени
const keyField = form.elements["key"];
// получение значения поля
console.log(keyField.type); // text
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Формы и их элементы](https://metanit.com/web/javascript/10.1.php)
Iepriekšēja lapa >>> [[Formas elementu iegūšana]]
Nākama lapa >>> [[Navigācija JavaScript]]

---