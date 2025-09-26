___

**Datums:** 2025-08-25
**Laiks:** 16:42
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Savu validācijas paziņojumu izveide

Lai veidot savus validācijas paziņojumus, metodei `setCustomValidity()` jānodot teksta virkni:

```html
<form id="registerForm" name="registerForm">
<p>
    <label for="username">Username:</label><br>
    <input id="username" name="username" maxlength="20" minlength="3" required>
</p>
<button type="submit" id="submit" name="submit">Register</button>
</form>
<script>
const registerForm = document.registerForm;
const submit = registerForm.submit;
submit.addEventListener("click", validate);
 
function validate(){
    if(registerForm.username.validity.valueMissing){
        registerForm.username.setCustomValidity("Необходимо ввести имя пользователя");
    }
    if(registerForm.username.validity.tooLong){
        registerForm.username.setCustomValidity("Имя пользователя не должно превышать 20 символов");
    }
    if(registerForm.username.validity.tooShort){
        registerForm.username.setCustomValidity("Имя пользователя не должно быть меньше 3 символов");
    }
}
</script>
```

![[Pasted image 20250825164427.png]]

---
### ⇄ Saistības

Avots >>> [JavaScript \| Управление валидацией форм](https://metanit.com/web/javascript/10.7.php)
Iepriekšēja lapa >>> [[Programmēšanas valodas/JavaScript (viss)/JavaScript/Darbs ar formām/Formu validācijas pārvaldība/Metodes|Metodes]]
Nākama lapa >>> [[Savu validācijas noteikumu izveide]]

---