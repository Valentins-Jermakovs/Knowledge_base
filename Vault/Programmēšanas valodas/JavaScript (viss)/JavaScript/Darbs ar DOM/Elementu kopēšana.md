___

**Datums:** 2025-08-17
**Laiks:** 14:41
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Elementu kopēšana

Dažreiz tiek izmantoti gna sarežģīti elementi pēc savas struktūras, daudz vieglāk būs to klonēt, nevis veidot jauno no atsevišķiem `html` tagiem.

Šim nolūkam tiek izmantota metode **cloneNode()**.

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
    // получаем последний параграф
    const lastP = article.lastElementChild;
    // клонируем элемент lastP
    const newLastP = lastP.cloneNode(true);
    // изменяем текст
    newLastP.textContent = "Publication Date: 28/10/2023";
    // добавляем в конец элемента article
    article.appendChild(newLastP);
    </script>
</body>
</html>
```

Kā parametrs metodei `cloneNode()` tiek nodota loģiska vērtība: ja tiek nodota vērtība `true`, elements tiks kopēts ar visiem bērnu mezgliem; ja tiek nodota vērtība `false`, tas tiks kopēts bez bērnu mezgliem.

Tas ir, šajā gadījumā mēs kopējam mezglu ar visu tā saturu un pēc tam pievienojam to elementa beigās ar `id="article"`.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Создание, добавление, замена и удаление элементов](https://metanit.com/web/javascript/8.5.php)
Iepriekšēja lapa >>> [[Elementu pievienošana]]
Nākama lapa >>> [[Elementu aizvietošana, maiņa]]

---