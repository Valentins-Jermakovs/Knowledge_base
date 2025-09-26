___

**Datums:** 2025-08-17
**Laiks:** 12:43
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Elementa meklēšana pēc `CSS` selektora

##### Metode `querySelector`

Elementa iegūšana pēc `CSS` selektora:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
    <div class="annotation">
        <p>Аннотация статьи</p>
    </div>
    <div class="text">
        <p>Первый абзац</p>
        <p>Второй абзац</p>
    </div>
    <script>
        const elem = document.querySelector(".annotation p");
        console.log(elem.innerText);    // Аннотация статьи
    </script>
</body>
</html>
```

Izteiksme `document.querySelector(".annotation p")` atrod elementu, kas atbilst selektoram `.annotation p`. <mark style="background: #FFB86CA6;">Ja lapā ir vairāki elementi, kas atbilst selektoram, metode atlasa pirmo no tiem.</mark>

##### Metode `querySelectorAll`

Lai iegūt visus elementus, kas atbilst `CSS` selektoram, izmanto metodi `querySelectorAll`, kas atgriež elementu sarakstu:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
    <div class="annotation">
        <p>Аннотация статьи</p>
    </div>
    <div class="text">
        <p>Первый абзац</p>
        <p>Второй абзац</p>
    </div>
    <script>
        const elems = document.querySelectorAll(".text p");
        for (elem of elems) {
            console.log(elem.innerText);
        }
    </script>
</body>
</html>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Поиск элементов на веб-странице](https://metanit.com/web/javascript/8.2.php)
Iepriekšēja lapa >>> [[Elementa iegūšana pēc atribūta name]]
Nākama lapa >>> [[Ielikto, child elementu meklēšana]]

---