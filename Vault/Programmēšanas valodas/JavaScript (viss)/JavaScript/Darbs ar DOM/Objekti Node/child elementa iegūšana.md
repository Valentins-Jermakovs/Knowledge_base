___

**Datums:** 2025-09-10
**Laiks:** 10:17
❚ **Tagi:** #javascript 

---
### `child` elementa iegūšana

Metode `hasChildNode()` atgriež `true`, ja elementam ir `child` mezgli.

```js
const article = document.querySelector("div");
if(article.hasChildNodes()){
    console.log("There are child nodes");
}
else{
    console.log("No child nodes");
}
```

Lai iegūt `child` elemtnus, var izmantot īpašību `children`:

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
// выбираем элемент c id="article"
const article = document.getElementById("article");
 
for(elem of article.children){
    console.log(elem);
}
</script>
</body>
</html>
```

Ja mums nepieciešams iegūt ne tikai `child` elementus, bet arī to atribūtus un tekstu, tad izmanto metodi `childNodes`:

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
// выбираем элемент c id="article"
const article = document.getElementById("article");
 
for(node of article.childNodes){
    let type = "";
    if(node.nodeType===1) type="элемент";
    else if(node.nodeType===2) type="атрибут";
    else if(node.nodeType===3) type="текст";
         
    console.log(node.nodeName, ": ", type);
}
</script>
</body>
</html>
```

Tā kā elementi neesot rakstīti vienā rindā, atdalīti ar `enter`, tad izvadā iegūstam:

```js
#text :  текст
H1 :  элемент
#text :  текст
P :  элемент
#text :  текст
```

Lai iegūt pirmo `child` elementu, izmanto šādas metodes:

- `firstChild`;
- `firstElementChild`.

Lai iegūt pēdējo `child` elementu, izmanto šādas metodes:

- `lastChild`;
- `lastElementChild`.

#### Elementu daudzums

Lai noteikt `child` elementu daudzumu, var izmantot īpašību `childelementCount`, kas ir ekvivalenta `children.length`:

```js
const article = document.getElementById("article");
console.log(article.childElementCount); // 2
console.log(article.children.length); // 2
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объект Node. Навигация по DOM](https://metanit.com/web/javascript/8.4.php)
Iepriekšēja lapa >>> [[parent elementa iegūšana]]
Nākama lapa >>> [[Viena līmeņa elementu iegūšana]]

---