___

**Datums:** 2025-08-25
**Laiks:** 14:53
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Elements `textarea`

Priekš vairāku rindu saturoša teksta lauka tiek izmantots tags `<textarea>`:

```html
<textarea rows="15" cols="40" name="textArea"></textarea>
```

Šis elements ģenerē tādus pašus notikumus kā standarta teksta lauks:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
</head>
<body>
<form name="search">
    <textarea rows="7" cols="40" name="message"></textarea>
</form>
<div id="printBlock"></div>
<script>
const messageBox = document.search.message;
 
// обработчик ввода символа
function onkeypress(e){
    // получаем элемент printBlock
    const printBlock = document.getElementById("printBlock");
    // получаем введенный символ
    const val = String.fromCharCode(e.keyCode);
    // добавление символа
    printBlock.textContent += val;
}
 
function onkeydown(e){
    if(e.keyCode===8){ // если нажат Backspace
     
        // получаем элемент printBlock
        const printBlock = document.getElementById("printBlock"), 
            length = printBlock.textContent.length;
        // обрезаем строку по последнему символу
        printBlock.textContent = printBlock.textContent.substring(0, length-1);
    }
}
 
messageBox.addEventListener("keypress", onkeypress);
messageBox.addEventListener("keydown", onkeydown);
</script>
</body>
</html>
```

Šī koda rinda konvertē klaviatūraws pogas kodu uz simbolu:

```js
const val = String.fromCharCode(e.keyCode);
```

Metode `keypress` - teksta simboli.
Metode `keydown` - simboli, kas ietekmē tekstu, piem., `Backspace`.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Текстовые поля](https://metanit.com/web/javascript/10.3.php)
Iepriekšēja lapa >>> [[Slēptais teksta lauks]]
Nākama lapa >>> [[Navigācija JavaScript]]

---