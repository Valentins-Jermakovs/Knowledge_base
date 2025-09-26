___

**Datums:** 2025-08-14
**Laiks:** 12:39
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Mainīgie un konstantes kā funkcijas

Mainīgiem un konstantēm var piešķirt arī funkcijas.

```js
function goodMorning(){
    console.log("Доброе утро");
}
function goodEvening(){
    console.log("Добрый вечер");
}
let message = goodMorning;      // присваиваем переменной message функцию goodMorning
message();      // Доброе утро
message = goodEvening;          // меняем функцию в переменной message
message();      // Добрый вечер
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Функции](https://metanit.com/web/javascript/3.1.php)
Iepriekšēja lapa >>> [[Funkcija]]
Nākama lapa >>> [[Anonīmas funkcijas]]

---