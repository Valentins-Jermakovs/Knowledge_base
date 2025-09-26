___

**Datums:** 2025-08-25
**Laiks:** 16:47
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Savu validācijas noteikumu izveide

Mēs neesam ierobežoti tikai ar atribūtiem. Veikt datu validāciju var arī caur saviem noteikumiem, vai pārbaudīt uz to pašu `regex`:

```html
<form id="registerForm" name="registerForm">
<p>
    <label for="username">Username:</label><br>
    <input id="username" name="username" maxlength="20" minlength="3" required>
</p>
<button type="submit" id="submit" name="submit">Register</button>
</form>
<script>
const usernameField = document.registerForm.username;
const submit = registerForm.submit;
submit.addEventListener("click", validate);
 
function validate(){
    if(usernameField.value === "admin"){
        usernameField.setCustomValidity("Недопустимое имя пользователя");
    }
}
</script>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Управление валидацией форм](https://metanit.com/web/javascript/10.7.php)
Iepriekšēja lapa >>> [[Savu validācijas paziņojumu izveide]]
Nākama lapa >>> [[Navigācija JavaScript]]

---