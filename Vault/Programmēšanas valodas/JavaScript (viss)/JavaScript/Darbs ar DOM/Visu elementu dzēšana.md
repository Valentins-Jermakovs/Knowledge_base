___

**Datums:** 2025-08-17
**Laiks:** 15:02
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Visu elementu dzēšana

Dažreiz rodas nepieciešamība izdēst visus elementus. Priekš tā izmanto ciklu:

```html
<div id="article">
    <h1>Home Page</h1>
    <p>Text 1</p>
    <p>Text 2</p>
</div>
<script>
const article = document.getElementById("article");
while(article.firstChild){
    article.removeChild(article.firstChild);
}
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Создание, добавление, замена и удаление элементов](https://metanit.com/web/javascript/8.5.php)
Iepriekšēja lapa >>> [[Visu elementu dzēšana]]
Nākama lapa >>> [[Navigācija JavaScript]]

---