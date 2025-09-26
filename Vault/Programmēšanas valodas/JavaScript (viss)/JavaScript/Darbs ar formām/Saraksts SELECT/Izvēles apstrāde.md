___

**Datums:** 2025-08-25
**Laiks:** 15:46
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Izvēles apstrāde

Elements `select` atbalsta notikumu `change` (izvēlēta elementa maiņa sarakstā jeb elements, ko izvēlējas lietotājs).

```html
<form name="myForm">
    <select name="language" size="5">
        <option value="JS" selected="selected">JavaScript</option>
        <option value="Java">Java</option>
        <option value="CS">C#</option>
        <option value="CPP">C++</option>
    </select>
</form>
<div id="selection"></div>
<script>
const languagesSelect = document.myForm.language;
const selection = document.getElementById("selection");
 
function changeOption(){
    const selectedOption = languagesSelect.options[languagesSelect.selectedIndex];
    selection.textContent = "Вы выбрали: " + selectedOption.text;
}
 
languagesSelect.addEventListener("change", changeOption);
</script>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Список select](https://metanit.com/web/javascript/10.5.php)
Iepriekšēja lapa >>> [[Dinamiska saraksta kontrole]]
Nākama lapa >>> [[Saraksts ar vairākām izvēlēm]]

---