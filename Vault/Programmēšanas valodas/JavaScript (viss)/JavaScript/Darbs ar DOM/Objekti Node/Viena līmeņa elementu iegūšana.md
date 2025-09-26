___

**Datums:** 2025-09-10
**Laiks:** 10:31
❚ **Tagi:** #javascript 

---
### Viena līmeņa elementu iegūšana

Lai iegūt iepriekšējos elementus, kas atrodas vienā līmenī ar esošu elementu, tiek izmantotas īpašības:

- `previousSibling`;
- `previousElementSibling`.

Lai iegūt nākamos elementus, kas atrodas vienā līmenī ar esošu elementu, tiek izmantotas īpašības:

- `nextSibling`;
- `nextElementSibling`.

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
        <p>Page Text 1</p>
        <p>Page Text 2</p>
        <p>Page Text 3</p>
    </div>
    <script>
    const article = document.getElementById("article");
    let tempNode = article.firstElementChild;
    while(tempNode != null){
        console.log(tempNode);
        tempNode = tempNode.nextElementSibling;
    }
    </script>
</body>
</html>
```

Iegūstam šādu konsoles izvadu:

```
<h1 id="header">Home Page</h1>
<p>Page Text 1</p>
<p>Page Text 2</p>
<p>Page Text 3</p>
```

Tas pats, ja iet no apakšēja elementa uz augšu:

```js
const article = document.getElementById("article");
let tempNode = article.lastElementChild;
while(tempNode != null){
    console.log(tempNode);
    tempNode = tempNode.previousElementSibling;
}
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объект Node. Навигация по DOM](https://metanit.com/web/javascript/8.4.php)
Iepriekšēja lapa >>> [[child elementa iegūšana]]
Nākama lapa >>> [[nodeValue un teksta satura iegūšana]]

---