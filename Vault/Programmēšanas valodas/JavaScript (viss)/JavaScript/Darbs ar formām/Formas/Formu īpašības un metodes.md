___

**Datums:** 2025-08-25
**Laiks:** 11:12
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Formu īpašības un metodes

Formai ir šādas īpašības:

| Īpašība    | Nozīme                                           |
| ---------- | ------------------------------------------------ |
| `name`     | formas nosaukumus                                |
| `elements` | formas elementu kolekcija                        |
| `length`   | formasd elementu daudzums                        |
| `action`   | adrese, uz kurieni tiek nosūtīta forma           |
| `method`   | HTTP metode, kas tiek izmantota datu nosūtīšanai |
Piemēram iegūsim formas īpašības:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
    <form id="search" name="search" action="https://google.com/search" method="get">
        <input type="text" id="key" name="q" />
        <input type="submit" id="send" name="send" />
    </form>
    <script>
    const form = document.getElementById("search");
    console.log(form.elements);     // HTMLFormControlsCollection(2) [input, input, q: input, send: input]
    console.log(form.length);       // 2
    console.log(form.name);         // search
    console.log(form.action);       // https://google.com/search
    console.log(form.method);       // get
    </script>
</body>
</html>
```

Starp metodēm vajag izcelt `submit` un `reset`:
- `submit` - nosūta datus uz serveri
- `reset` - attīra ievades laukus

```js
const form = document.forms["search"];
form.submit();
form.reset();
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Формы и их элементы](https://metanit.com/web/javascript/10.1.php)
Iepriekšēja lapa >>> [[Formas iegūšana]]
Nākama lapa >>> [[Formas elementu iegūšana]]

---