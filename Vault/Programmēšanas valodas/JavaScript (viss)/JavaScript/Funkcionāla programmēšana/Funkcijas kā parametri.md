___

**Datums:** 2025-08-14
**Laiks:** 15:53
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Funkcijas kā parametri

Funkcijai parametros var nodot ne tikai mainīgos un vērtības, bet arī citas funkcijas.

```js
function sum(x, y){
    return x + y;
}
 
function subtract(x, y){
    return x - y;
}
 
function operation(x, y, func){
  
    const result = func(x, y);
    console.log(result);
}
 
console.log("Sum");
operation(10, 6, sum);  // 16
 
console.log("Subtract");
operation(10, 6, subtract); // 4
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Параметры функции](https://metanit.com/web/javascript/3.10.php)
Iepriekšēja lapa >>> [[Neobligāti parametri, noklusējuma vērtības]]
Nākama lapa >>> [[Funkcijas rezultāts]]

---