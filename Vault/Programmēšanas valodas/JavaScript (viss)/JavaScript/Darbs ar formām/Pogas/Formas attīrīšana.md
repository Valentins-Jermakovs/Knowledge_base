___

**Datums:** 2025-08-25
**Laiks:** 11:51
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Formas attīrīšana

Lai attīrītu formu, tiek izmantotas viena no šādam pogām:

```js
<button type="reset">Очистить</button>
<input type="reset" value="Очистить" />
```

Nospiežot šādu pogu, forma tiks attīrīta, taču šādu funkcionālu var izveidot caur metodi `reset()`:

```js
function sendForm(e){
     
    // получаем значение поля key
    const keyBox = document.search.key;
    const val = keyBox.value;
    if(val.length < 3){
        alert("Недопустимая длина строки");
        document.search.reset();
        e.preventDefault();
    }   
    else
        alert("Отправка разрешена");
}
```

Otrs veids kā attīrīt formas elementa saturu ir manuāli attīrīt `value`.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Кнопки](https://metanit.com/web/javascript/10.2.php)
Iepriekšēja lapa >>> [[Datu nosūtīšana]]
Nākama lapa >>> [[Navigācija JavaScript]]

---