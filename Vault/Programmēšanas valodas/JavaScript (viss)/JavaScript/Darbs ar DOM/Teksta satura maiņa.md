___

**Datums:** 2025-08-17
**Laiks:** 14:11
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Teksta satura maiņa

Šeit tiek demonstrēts, kā izmantojot īpašību `innerText`, var mainīt tekstisko saturu `HTML` elementiem:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
    <h1 id="header">Home Page</h1>
    <script>
    const header = document.getElementById("header");
    // получаем текст элемента
    console.log(header.innerText);  // Home Page
    // изменяем текст элемента
    header.innerText = "Hello World2";
    </script>
</body>
</html>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Элементы](https://metanit.com/web/javascript/8.6.php)
Iepriekšēja lapa >>> [[Objekts Node, navigācija pa DOM]]
Nākama lapa >>> [[HTML koda maiņa]]

---