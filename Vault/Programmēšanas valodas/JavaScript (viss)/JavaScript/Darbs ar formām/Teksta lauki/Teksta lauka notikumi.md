___

**Datums:** 2025-08-25
**Laiks:** 14:35
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Teksta lauka notikumi

Teksta lauks atbalsta šādus notikumus:

- `focus` - notiek, kad ir fokusējums
- `blur` - notiek, kad fokusējums tiek zaudēts
- `change` - notiek, kad tiek mainīta teksta lauka vērtība
- `input` - notiek, kad tiek mainīta teksta lauka vērtība
- `select` - notiek, kad tiek iezīmēts teksts teksta laukā
- `keydown` - notiek, kad nospiež klaviatūras pogu
- `keypress` - notiek, kad nospiež klaviatūras rakstu simbolu pogu
- `keyup` - notiek, kad atlaiž klaviatūras nospiesto pogu

Piemērs ar simbolu izmantošanu:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
</head>
<body>
<form name="search">
    <input type="text" name="key" placeholder="Введите ключ" />
    <input type="button" name="print" value="Печать" />
</form>
<div id="printBlock"></div>
<script>
const keyBox = document.search.key;
 
// обработчик изменения текста
function onchange(e){
    // получаем элемент printBlock
    const printBlock = document.getElementById("printBlock");
    // получаем новое значение
    const val = e.target.value;
    // установка значения
    printBlock.textContent = val;
}
// обработка потери фокуса
function onblur(e){
     
    // получаем его значение и обрезаем все пробелы
    const text = keyBox.value.trim();
    if(text==="")
        keyBox.style.borderColor = "red";
    else
        keyBox.style.borderColor = "green";
}
// получение фокуса
function onfocus(e){
     
    // установка цвета границ поля
    keyBox.style.borderColor = "blue";
}
keyBox.addEventListener("change", onchange);
keyBox.addEventListener("blur", onblur);
keyBox.addEventListener("focus", onfocus);
</script>
</body>
</html>
```

Šajā piemērā varētu izmantot notikumu `input`, bet no `change` tas atšķiras ar to, ka tas darbojas uzreiz, kā notiek teksta ievade, no pirmā simbolā.
`change` nostrādā, kad ievade tiek pabeigta un lietotājs noņen fokusējumu no teksta lauka.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Текстовые поля](https://metanit.com/web/javascript/10.3.php)
Iepriekšēja lapa >>> [[Teksta lauka izveide]]
Nākama lapa >>> [[Paroles ievades lauks]]

---