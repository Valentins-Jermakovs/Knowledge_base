___

**Datums:** 2025-08-25
**Laiks:** 11:44
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Datu nosūtīšana

Nospiežot pogu (`<button>` vai `<input>)`), dati tiek nosūtīti uz lapas adresi, ja atribūts `action` nav norādīts, taču `JavaScript` ļauj mums bloķēt datu nosūtīšanu, ja, piem., neatbilst mūsu nosacījumiem.

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
</head>
<body>
<form name="search">
    <input type="text" name="key"></input>
    <input type="submit" name="send" value="Отправить" />
</form>
<script>
function sendForm(e){
     
    // получаем значение поля key
    const keyBox = document.search.key;
    const val = keyBox.value;
    if(val.length<3){
        alert("Недопустимая длина строки");
        e.preventDefault();
    }   
    else
        alert("Отправка разрешена");
}
 
const sendButton = document.search.send;
sendButton.addEventListener("click", sendForm);
</script>
</body>
</html>
```

Metode `e.preventDefault()` ļauj bloķēt datu nosūtīšanu. `e` ir notikums.
Ja dati iziet validāciju, tad tiek parādīts `alert` paziņojums:

![[Pasted image 20250825114726.png]]

Papildus mēs varam arī mainīt adresi, uz kuru tiek nosūtīti formas dati. Šeit dati tiek pārvirzīti uz `PostForm`:

```js
function sendForm(e){
     
    // получаем значение поля key
    const keyBox = document.search.key;
    const val = keyBox.value;
    if(val.length > 3){
        alert("Недопустимая длина строки");
        document.search.action="PostForm";
    }   
    else
        alert("Отправка разрешена");
}
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Кнопки](https://metanit.com/web/javascript/10.2.php)
Iepriekšēja lapa >>> [[Pogas izveide]]
Nākama lapa >>> [[Formas attīrīšana]]

---