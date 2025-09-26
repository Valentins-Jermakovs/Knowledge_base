___

**Datums:** 2025-08-17
**Laiks:** 12:30
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Elementa iegūšana pēc `taga`

Meklēšana pēc noteiktā taga:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
    <h1>Home Page</h1>
    <p>Первый абзац</p>
    <p>Второй абзац</p>
    <script>
        const paragraphs = document.getElementsByTagName("p");
  
        for (p of paragraphs) {
            console.log(p.innerText);   // выводим текст параграфа
        }
    </script>
</body>
</html>
```

Šeit tiek atrgiezts masīvs no `<p>` taga elementiem. Tas nozīmē, kā pa šo masīvu var iterēt, izmantojot `for` ciklu, bet, ja vajag piekļūt pie konkrēta elementa, tad izmanot indeksus.

```js
const p = document.getElementsByTagName("p")[0];
console.log(p.innerText);
```

Tāpat šeit darbojas masīvu metodes.

```js
const paragraphs = document.getElementsByTagName("p");
console.log(paragraphs.length);
```

```js
const paragraphs = document.getElementsByTagName("p");
for (let i=0; i < paragraphs.length; i++) {
    console.log(paragraphs[i].innerText);
}
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Поиск элементов на веб-странице](https://metanit.com/web/javascript/8.2.php)
Iepriekšēja lapa >>> [[Elementa iegūšana pēc id]]
Nākama lapa >>> [[Elementa iegūšana pēc klases]]

---