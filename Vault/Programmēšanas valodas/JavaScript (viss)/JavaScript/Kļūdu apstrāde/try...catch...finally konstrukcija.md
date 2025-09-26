___

**Datums:** 2025-08-16
**Laiks:** 14:25
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### `try...catch...finally` konstrukcija

Šī konstrukcija satāv no 3 blokiem:

- `try` - šeit tiek aprakstīts kods, kas potenciāli var izraisīt kļūdas;
- `catch` - bloks, kas nostrādā, ja notiek kļūda;
- `finally` - bloks, kas izpildās neatkarīgi no tā bija kļūda vai nē.

```js
try{
    callSomeFunc();
    console.log("Конец блока try");
}
catch{
    console.log("Возникла ошибка!");
}
console.log("Остальные инструкции");
```

##### Kļūdas iegūšana blokā `catch`

```js
try{
    callSomeFunc();
    console.log("Конец блока try");
}
catch(error){
    console.log("Возникла ошибка!");
    console.log(error);
}
```

```
Возникла ошибка!
ReferenceError: callSomeFunc is not defined
    at index.html:35
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Конструкция try..catch..finally](https://metanit.com/web/javascript/16.1.php)
Iepriekšēja lapa >>> [[Navigācija JavaScript]]
Nākama lapa >>> [[Kļūdu ģenerēšana un operators throw]]

---