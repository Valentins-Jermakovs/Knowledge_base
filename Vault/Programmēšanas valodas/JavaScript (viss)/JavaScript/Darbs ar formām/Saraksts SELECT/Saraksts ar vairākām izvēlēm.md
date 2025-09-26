___

**Datums:** 2025-08-25
**Laiks:** 15:58
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Saraksts ar vairākām izvēlēm

Ja sarakstam pievienots atribūts `multiple`, tad, lai iegūt lietotāja izvēlētos elementus, tiek izmantota īpašība `selectedOptions`, kas atgriež izvēlēto elementu sarakstu. Lai izvēlēties vairākus elementus, izmanto `shift` vai `ctrl` pogu kopā ar peli.

```html
<form name="myForm">
    <select name="languages" multiple>
        <option value="JS">JavaScript</option>
        <option value="Java">Java</option>
        <option value="CS">C#</option>
        <option value="CPP">C++</option>
    </select>
</form>
<div id="selection"></div>
<script>
const languages = document.myForm.languages;
const selection = document.getElementById("selection");
 
function changeOption(){
    // удаляем ранее выбранные элементы
    while (selection.firstChild) { 
        selection.removeChild(selection.firstChild);  
    }
    // получаем выбранные элементы 
    const options = languages.selectedOptions;
    for (let i = 0; i < options.length; i++) {      // for each option ...    
        const option = options[i].text    // получаем выбранный элемент 
        const div = document.createElement("div");  // для каждого выбранного элемента создаем div
        const optionText = document.createTextNode(option); // создаем текстовый узел для выбранного элемента  
        div.appendChild(optionText);    // добавляем  optionText в div   
        selection.appendChild(div)      // добавляем div в контейнер
    }
}
languages.addEventListener("change", changeOption);
</script>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Список select](https://metanit.com/web/javascript/10.5.php)
Iepriekšēja lapa >>> [[Izvēles apstrāde]]
Nākama lapa >>> [[Navigācija JavaScript]]

---