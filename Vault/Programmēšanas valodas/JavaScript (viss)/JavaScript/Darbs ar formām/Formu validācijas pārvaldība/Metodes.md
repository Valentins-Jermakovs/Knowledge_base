___

**Datums:** 2025-08-25
**Laiks:** 16:38
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Metodes

Ir šādas metodes, kas ļauj kontrolēt formu validāciju:

- `checkValidity()` - pārbauda, vai forma vai norādītais elements iziet datu validāciju. Ja viss labi, tad `true`, pretēji `false`.
- `reportValidity()` - dara to pašu, bet atgriež arī validācijas kļūdas.
- `setCustomValidity()` - šī metode ļauj izveidot savu validācijas paziņojumu.

```html
<form id="registerForm" name="registerForm" method="post" action="register">
<p>
    <label for="username">Username:</label><br>
    <input id="username" name="username" maxlength="20" minlength="3" required>
</p>
<p>
    <label for="age">Age:</label><br>
    <input type="number" id="age" name="age" min="1" max="110" required>
</p>
<button type="submit" id="submit" name="submit">Register</button>
</form>
<script>
const registerForm = document.registerForm;
const submit = registerForm.submit;
submit.addEventListener("click", validate);
 
function validate(){
    if(!registerForm.username.checkValidity()){
        console.log("Username is not valid");
    }
    if(!registerForm.age.checkValidity()){
        console.log("Age is not valid");
    }
    if(!registerForm.checkValidity()){
        console.log("Form data is not valid");
    }
}
</script>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Управление валидацией форм](https://metanit.com/web/javascript/10.7.php)
Iepriekšēja lapa >>> [[Navigācija JavaScript]]
Nākama lapa >>> [[Savu validācijas paziņojumu izveide]]

---