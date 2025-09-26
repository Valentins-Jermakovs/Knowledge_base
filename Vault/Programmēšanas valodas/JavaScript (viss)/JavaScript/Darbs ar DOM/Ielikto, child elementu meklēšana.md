___

**Datums:** 2025-08-17
**Laiks:** 12:49
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Tēma

Piemērs, kur parādīts, kā var piekļūt pie `child` tipa elementiem:

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
        <p class="text">Page Text 1</p>
        <p class="text">Page Text 2</p>
    </div>
    <div id="footer">
        <p class="text">Footer Text</p>
    </div>
    <script>
    // получаем элемент с id="article"
    const article = document.getElementById("article");
    // в этом элементе получаем все элементы с class="text"
    const articleContent = article.getElementsByClassName("text");
    for(p of articleContent){
        console.log(p);
    }
    </script>
</body>
</html>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Поиск элементов на веб-странице](https://metanit.com/web/javascript/8.2.php)
Iepriekšēja lapa >>> [[Elementa meklēšana pēc CSS selektora]]
Nākama lapa >>> [[Navigācija JavaScript]]

---