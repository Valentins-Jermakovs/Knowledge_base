___

**Datums:** 2025-08-25
**Laiks:** 14:45
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Paroles ievades lauks

Paroles ievadam tiek izmantots lauks `<input type="password"/>`. Parole nekādi netiek šifrēta, to slēpj zem maskas, lauka saturu var gana vienkārsi nolasīt:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
 <form name="loginForm">
    <input type="password" name="password" />
</form>
<div id="printBlock"></div>
<script>
const passwordBox = document.loginForm.password;
  
// обработчик изменения текста
function oninput(e){
    // получаем элемент printBlock
    const printBlock = document.getElementById("printBlock");
    // получаем новое значение
    printBlock.textContent = e.target.value;
} 
passwordBox.addEventListener("input", oninput); 
</script>
</body>
</html>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Текстовые поля](https://metanit.com/web/javascript/10.3.php)
Iepriekšēja lapa >>> [[Teksta lauka notikumi]]
Nākama lapa >>> [[Slēptais teksta lauks]]

---