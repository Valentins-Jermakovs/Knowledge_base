___

**Datums:** 2025-08-19
**Laiks:** 15:40
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Notikumu klausītāja pievienošana

Lai strādātu ar notikumu klausītājiem, JavaScript valodā ir `EventTarget` objekts, kas definē metodes. Viena no tām ir `addEventListener()`, kas ļauj pievienot notikuma apstrādātāju kādam `html` objektam.

Metode pieņem divus parametrus:

- notikuma apstrādātāju bez prefiksa **on**;
- funkciju, kas tiks izsaukta notikuma laikā.

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
    <button id="btn">Click Me</div>
    <script>
    let clicks = 0;     // счетчик нажатий
    function btn_click(){
        console.log("Clicked", ++clicks);
    }
    const btn = document.getElementById("btn");
    // прикрепляем обработчик события "click"
    btn.addEventListener("click", btn_click);
    </script>
</body>
</html>
```

#### Notikuma klausītāja dzēšana

Dzēšana ir analoģiska pievienošanai:

```js
rect.removeEventListener("click", btn_click);
```

#### Vairāku notikumu klausītāju pievienošana

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
    <button id="btn">Click Me</div>
    <script>
    let clicks = 0;     // счетчик нажатий
    function btn_click(){
        console.log("Clicked", ++clicks);
    }
    const btn = document.getElementById("btn");
 
    // прикрепляем первый обработчик события "click" в виде функции btn_click
    btn.addEventListener("click", btn_click);
 
    // прикрепляем второй обработчик события "click" в виде анонимной функции
    btn.addEventListener("click", function(){
        console.log("Button clicked!")
    });
 
    // прикрепляем третий обработчик события "click" в виде стрелочной функции
    btn.addEventListener("click", ()=>console.log("Element clicked!"));
 
    </script>
</body>
</html>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Обработчики событий](https://metanit.com/web/javascript/9.2.php)
Iepriekšēja lapa >>> [[Navigācija JavaScript]]
Nākama lapa >>> [[MouseEvent]]

---