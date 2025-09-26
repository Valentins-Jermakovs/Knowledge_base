___

**Datums:** 2025-08-25
**Laiks:** 15:11
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Radiopogas

Atšķirībā no `checkbox`, radiopogas atļauj izvēlēties tikai vienu opciju. Radiopogu izveido elements `<input type="radio">`. Radiopogas izvēle ir `click` notikums:

```html
<form name="myForm">
    <input type="radio" name="languages" value="Java" /><span>Java</span>
    <input type="radio" name="languages" value="C#" /><span>C#</span>
    <input type="radio" name="languages" value="C++" /><span>C++</span>
</form>
<div id="printBlock"></div>
<script>
const printBlock = document.getElementById("printBlock");
const myForm = document.myForm;
function onclick(e){
    printBlock.textContent = `Вы выбрали: ${myForm.languages.value}`;
}
for (let i = 0; i < myForm.languages.length; i++) {
    myForm.languages[i].addEventListener("click", onclick);
}
</script>
```

<mark style="background: #FFB86CA6;">Visām radiopogām `name` atribūtam jābut vienādam!</mark>

Tāpāt kā `checkbox` elementiem, radiopogām ir īpašība `checked`, kas atgriež `true`:

```js
myForm.languages[myForm.languages.length-1].checked = true;
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Флажки и радиокнопки](https://metanit.com/web/javascript/10.4.php)
Iepriekšēja lapa >>> [[Karogi]]
Nākama lapa >>> [[Navigācija JavaScript]]

---