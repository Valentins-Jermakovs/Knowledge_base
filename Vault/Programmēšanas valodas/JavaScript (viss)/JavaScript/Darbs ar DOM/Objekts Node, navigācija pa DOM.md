___

**Datums:** 2025-08-17
**Laiks:** 13:56
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Objekts `Node`

| Īpašība                    | Apraksts                                                                |
| -------------------------- | ----------------------------------------------------------------------- |
| **childNodes**             | Satur kolekciju ar visiem bērnu mezgliem                                |
| **children**               | Satur kolekciju ar bērnu mezgliem, kas ir elementi                      |
| **firstChild**             | Atgriež pirmo pašreizējā mezgla bērnu mezglu                            |
| **firstElementChild**      | Atgriež pirmo bērnu mezglu, kas ir elements                             |
| **lastChild**              | Atgriež pēdējo pašreizējā mezgla bērnu mezglu                           |
| **lastElementChild**       | Atgriež pēdējo bērnu mezglu, kas ir elements                            |
| **previousSibling**        | Atgriež iepriekšējo mezglu tajā pašā līmenī                             |
| **nextSibling**            | Atgriež nākamo mezglu tajā pašā līmenī                                  |
| **previousElementSibling** | Atgriež iepriekšējo mezglu, kas ir elements un atrodas tajā pašā līmenī |
| **nextElementSibling**     | Atgriež nākamo mezglu, kas ir elements un atrodas tajā pašā līmenī      |
| **ownerDocument**          | Atgriež dokumenta saknes mezglu                                         |
| **parentNode**             | Atgriež pašreizējā mezgla vecāku mezglu                                 |
| **parentElement**          | Atgriež vecāku mezglu, kas ir elements                                  |
| **nodeName**               | Atgriež mezgla nosaukumu                                                |
| **nodeType**               | Atgriež mezgla tipu skaitļa veidā                                       |
| **nodeValue**              | Atgriež teksta mezgla tekstu (saturu)                                   |

Izmantošanas piemērs, `child` elementu iegūšana:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
    <div id="article">
        <h1 id="header">Home Page</h1>
        <p>Page Text</p>
    </div>
    <script>
    // выбираем все элемент c id="header"
    const header = document.getElementById("header");
    // получаем родительский элемента
    const headerParent = header?.parentElement;
    // можно так
    // const headerParent = header?.parentNode;
    console.log(headerParent);    // выводим родительский элемент на консоль
    </script>
</body>
</html>
```

Šeit tiek izmantots operators `?`, kas darbojas kā aizsardzība pret to, ja meklējamais elemets/i neeksistē. Burtiskis - *atrodi elementu, ja tas eksistē.*
Šāds operators nav obligāts, var iegūt elemntu vienkārši caur punktu.

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
    <div id="article">
        <h1 id="header">Home Page</h1>
        <p id="text">Page Text</p>
    </div>
    <script>
    // получаем элемент с id="text"
    const pageText = document.getElementById("text");
    console.log(pageText.nodeValue);    // null 
    for(textNode of pageText.childNodes){
        console.log(textNode.nodeValue);
    }
    </script>
</body>
</html>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объект Node. Навигация по DOM](https://metanit.com/web/javascript/8.4.php)
Iepriekšēja lapa >>> [[Navigācija JavaScript]]
Nākama lapa >>> [[Teksta satura maiņa]]

---