___

**Datums:** 2025-08-17
**Laiks:** 14:54
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Elementu aizvietošana

Lai aizvietot vienu elementu ar kādu citu elementu, tiek izmantota metode `replaceChild(newNode, oldNode)`, kas pieņem divus parametrus:

- `newNode` - jaunais elements, kas aizvieto veco;
- `oldNode` - vecais elements, kas tiks aizvietots.

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
    <div id="article">
        <p>Home Page</p>
        <p>Text 1</p>
        <p>Text 2</p>
    </div>
    <script>
    const article = document.getElementById("article");
    // находим узел, который будем заменять
    // пусть это будет первый элемент
    const oldNode = article.firstElementChild;
    // создаем новый элемент
    const newNode = document.createElement("h2");
    // определяем для него текст
    newNode.textContent = "Hello World";
    // заменяем старый узел новым
    article.replaceChild(newNode, oldNode);
    </script>
</body>
</html>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Создание, добавление, замена и удаление элементов](https://metanit.com/web/javascript/8.5.php)
Iepriekšēja lapa >>> [[Elementu kopēšana]]
Nākama lapa >>> [[Elementu dzēšana]]

---