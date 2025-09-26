___

**Datums:** 2025-08-17
**Laiks:** 14:15
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### HTML koda maiņa

Lai mainīt kodu kādam `html` elementam, tiek izmantota īpašība `innerHTML`:

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
    // получаем html-код элемента
    console.log(header.innerHTML);  // Home Page
    // изменяем html-код элемента
    header.innerHTML = "<span style='color:navy;'>Hello World</span>";
    </script>
</body>
</html>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Элементы](https://metanit.com/web/javascript/8.6.php)
Iepriekšēja lapa >>> [[Teksta satura maiņa]]
Nākama lapa >>> [[Navigācija JavaScript]]

---