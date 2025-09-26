___

**Datums:** 2025-08-17
**Laiks:** 12:35
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Elementa iegūšana pēc `klases`

Elementu iegūšana pēc klases, šeit tāpat kā ar tagiem, tiek atgriezts elementu masīvs:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
    <h1>Home Page</h1>
    <p class="text">Page Text</p>
    <p class="contacts">Email: supercorp@zmail.com</p> 
    <p class="contacts">Phone: +1-234-567-8901</p>
    <script>
        const contacts = document.getElementsByClassName("contacts");
  
        for (contact of contacts) {
            console.log(contact.innerText);
        }
    </script>
</body>
</html>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Поиск элементов на веб-странице](https://metanit.com/web/javascript/8.2.php)
Iepriekšēja lapa >>> [[Elementa iegūšana pēc taga]]
Nākama lapa >>> [[Elementa iegūšana pēc atribūta name]]

---