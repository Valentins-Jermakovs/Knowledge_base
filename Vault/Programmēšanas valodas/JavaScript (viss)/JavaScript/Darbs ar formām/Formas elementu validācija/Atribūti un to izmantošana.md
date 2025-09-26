___

**Datums:** 2025-08-25
**Laiks:** 16:21
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Atribūti un to izmantošana

`HTML` atbalsta atribūtus, kas tiek izmantoti formas validācijai:

- `required` - obligats aizpildei, atzimēšanai
- `max` - nosaka maksimālu skaitlisko vērtību
- `min` - nosaka minimālu skaitlisko vērtību
- `maxlength` - nosaka maksimālu teksta virknes garumu
- `minlength` - nosaka minimāļu teksta virknes garumu

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
    <style>
    input {width: 150px;}
    input:invalid {border-color: red; }
    input:valid { border-color: green;}
    </style>
</head>
<body>
<form id="registerForm" name="registerForm" method="post" action="register">
<p>
    <label for="username">Username:</label><br>
    <input id="username" name="username" maxlength="20" minlength="3" required>
</p>
<p>
    <label for="email">Email:</label><br>
    <input type="email" id="email" name="email" required>
</p>
<p>
    <label for="age">Age:</label><br>
    <input type="number" id="age" name="age" min="1" max="110" value="18">
</p>
<button type="submit" id="submit" name="submit">Register</button>
</form>
</body>
</html>
```

Šīs koda rindas nosaka elementu stilu pēc to validācijas:

```css
input:invalid {border-color: red; }
input:valid { border-color: green;}
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Validation API. Валидация элементов формы](https://metanit.com/web/javascript/10.6.php)
Iepriekšēja lapa >>> [[Navigācija JavaScript]]

---