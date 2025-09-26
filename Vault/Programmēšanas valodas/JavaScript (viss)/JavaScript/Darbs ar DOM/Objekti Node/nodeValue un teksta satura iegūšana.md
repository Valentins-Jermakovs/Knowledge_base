___

**Datums:** 2025-09-10
**Laiks:** 10:37
❚ **Tagi:** #javascript 

---
### nodeValue un teksta satura iegūšana

Īpašība `nodeValue` ļauj iegūt teksta elementa saturu, tā tekstu:

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

šeit pēc elementa `<p>` saglabāšānas konstantē mēs mēģinām piekļūt pie tā satura un iegūstam `null`, jo teksts jau arī ir `node` elements. Teksts šajā piemēra ir `child` elements tagam `<p>`.

Konsoles izvadā būs:

```
null
Page Text
```

Tas nav labakais veids, kā iegūt teksta saturu, vienkāršāk vērsties pa taisno caur `textContent` vai tml.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объект Node. Навигация по DOM](https://metanit.com/web/javascript/8.4.php)
Iepriekšēja lapa >>> [[Viena līmeņa elementu iegūšana]]
Nākama lapa >>> [[Navigācija - Objekti Node]]

---