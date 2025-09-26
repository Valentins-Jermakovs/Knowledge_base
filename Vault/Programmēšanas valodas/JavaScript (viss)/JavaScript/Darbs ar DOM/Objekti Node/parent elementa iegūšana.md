___

**Datums:** 2025-09-10
**Laiks:** 10:12
❚ **Tagi:** #javascript 

---
### `parent` elementa iegūšana

Lai iegūt `parent` elementu, tiek izmantotas metodes:

- `parentNode` - atgriež `parent` mezglu;
- `parentElement` - atgriež `parent` elementu.


```js
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

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объект Node. Навигация по DOM](https://metanit.com/web/javascript/8.4.php)
Iepriekšēja lapa >>> [[nodeName un nodeType]]
Nākama lapa >>> [[child elementa iegūšana]]

---