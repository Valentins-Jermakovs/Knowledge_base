___

**Datums:** 2025-08-25
**Laiks:** 15:07
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Karogi

Karogi ir tāds lauks, kuru var atzimēt izvēlētu, to veido izmantojot `<input type="checkbox">`. Tam ir īpašība `checked`, kas atgriež `true`:

```html
<form name="myForm">
    <input type="checkbox" name="enabled" checked><span>Включить</span>
</form>
<div id="printBlock"></div>
<script>
const enabledBox = document.myForm.enabled;
const printBlock = document.getElementById("printBlock");
//  в текст printBlock передаем установленное значение
enabledBox.addEventListener("click", (e)=> printBlock.textContent = e.target.checked);
</script>
```

`checkbox` ļauj izvēlēties vairākus atbilžu variantus, kas tiek piedāvāti lietotājam.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Флажки и радиокнопки](https://metanit.com/web/javascript/10.4.php)
Iepriekšēja lapa >>> [[Navigācija JavaScript]]
Nākama lapa >>> [[Radiopogas]]

---