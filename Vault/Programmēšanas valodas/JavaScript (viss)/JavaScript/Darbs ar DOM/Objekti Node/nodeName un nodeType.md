___

**Datums:** 2025-09-10
**Laiks:** 10:08
❚ **Tagi:** #javascript 

---
### nodeName un nodeType

Lai uzzināta `node` tipu, mēs varam izmantot metodes:

- `nodeName`;
- `nodeType`.

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
const article = document.getElementById("article");
console.log(article.nodeName);  // DIV
console.log(article.nodeType);  // 1
</script>
</body>
</html>
```

Metode `nodeName` atgriež `node` taga nosaukumu.
Metode `nodeType` atgriež `node` ciparu `1`, kas nozīmē ka objekts ir elements.

| nodeType | Mezgla tips |
| -------- | ----------- |
| 1        | elements    |
| 2        | atribūts    |
| 3        | teksts      |

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объект Node. Навигация по DOM](https://metanit.com/web/javascript/8.4.php)
Iepriekšēja lapa >>> [[node īpašības]]
Nākama lapa >>> [[parent elementa iegūšana]]

---