___

**Datums:** 2025-08-17
**Laiks:** 12:37
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Elementa iegūšana pēc atribūta `name`

Metode `getElementsByName()` ļauj iegūt elementu sarakstu pēc `name` - nosaukuma atribūta. **Šī metode tiek lietota formas elementiem.** Piemēram:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
    <form>
        <p>Language:</p>
        <input type="radio" name="lang" value="Java">
        <label>Java</label>
        <br>
        <input type="radio" name="lang" value="JavaScript" checked>
        <label>JavaScript</label>
        <br>
        <input type="radio" name="lang" value="PHP">
        <label>PHP</label>
        <br>
    </form>
    <script>
    // выбираем все элементы с атрибутом name="lang"
    const langs = document.getElementsByName("lang");
    for (lang of langs) {
        console.log(lang.value);    // получаем значение атрибута value
    }
    </script>
</body>
</html>
```

Šeit arī tiek atgriezts elementu masīvs. Lai izvadīt elementa `lang` saturu, tiek izmantota `value` īpašība.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Поиск элементов на веб-странице](https://metanit.com/web/javascript/8.2.php)
Iepriekšēja lapa >>> [[Elementa iegūšana pēc klases]]
Nākama lapa >>> [[Elementa meklēšana pēc CSS selektora]]

---