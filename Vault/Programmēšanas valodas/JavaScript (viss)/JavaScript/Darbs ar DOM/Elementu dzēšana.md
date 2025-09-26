___

**Datums:** 2025-08-17
**Laiks:** 15:00
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Elementa dzēšana

Elementa/u dzēšanai tiek izmantota metode **removeChild()**. Šī metode dzēš `child` elementu/mezglu, kā parametru pieņem dzēšamo elementu:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
    <div id="article">
        <h1>Home Page</h1>
        <p>Text 1</p>
        <p>Text 2</p>
    </div>
    <script>
    const article = document.getElementById("article");
    // находим узел, который будем удалять - последний параграф
    const lastP = article.lastElementChild;
    // удаляем узел
    article.removeChild(lastP);
    </script>
</body>
</html>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Создание, добавление, замена и удаление элементов](https://metanit.com/web/javascript/8.5.php)
Iepriekšēja lapa >>> [[Elementu aizvietošana, maiņa]]
Nākama lapa >>> [[Visu elementu dzēšana]]

---