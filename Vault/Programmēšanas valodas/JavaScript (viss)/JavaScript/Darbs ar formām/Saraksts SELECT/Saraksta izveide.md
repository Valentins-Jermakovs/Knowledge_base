___

**Datums:** 2025-08-25
**Laiks:** 15:33
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Saraksta izveide

Saraksta izveides piemērs:

```html
<select name="language" size="4">
    <option value="JS" selected="selected">JavaScript</option>
    <option value="Java">Java</option>
    <option value="C#">C#</option>
    <option value="C++">C++</option>
</select>
```

Par saraksta atribūtiem:

- `size` - ja vienāds ar 1, saraksts būs izkritošais, attēlo tikai vienu elementu
- `multiple` - ja šis atribūts esot iestatīts, tad var veikt vairākas izvēles

Saraksta elementus var iegūt caur `options`, nododot indeksu:

```html
<form name="myForm">
    <select name="language" size="4">
        <option value="JS" selected="selected">JavaScript</option>
        <option value="Java">Java</option>
        <option value="CS">C#</option>
        <option value="CPP">C++</option>
    </select>
</form>
<script>
const firstLanguage = document.myForm.language.options[0];
console.log("Index:", firstLanguage.index);
console.log("Text:", firstLanguage.text);
console.log("Value:", firstLanguage.value);
</script>
```

Saraksta elementus var iegūt caur `items()`, nododot indeksu:

```js
const firstLanguage = myForm.language.item(0);
console.log("Index:", firstLanguage.index);
console.log("Text:", firstLanguage.text);
console.log("Value:", firstLanguage.value);
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Список select](https://metanit.com/web/javascript/10.5.php)
Iepriekšēja lapa >>> [[Navigācija JavaScript]]
Nākama lapa >>> [[Dinamiska saraksta kontrole]]

---