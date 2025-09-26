___

**Datums:** 2025-08-14
**Laiks:** 16:25
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Rekursīvas funkcijas

Tas ir tādas funkcijas, kas ir spējīgas izsaukt pašas sevi darbības rezultātā. Piemēram, funkcija, kas aprēķina faktoriālu:

```js
function factorial(n){
    if (n === 1){
        return 1;
    }
    else{
         
        return n * factorial(n - 1);
    }
}
const result = factorial(4); 
console.log(result); // 24
```

Tā izpildās šādā secībā:

```js
result = 4 * factorial(3);
result = 4 * 3 * factorial(2);
result = 4 * 3 * 2 * factorial(1);
result = 4 * 3 * 2 * 1; // 24
```

Cits piemērs:

```js
function fibonachi(n)
{
    if (n === 0 || n === 1){
        return n;
    }
    else{
        return fibonachi(n - 1) + fibonachi(n - 2);
    }
}
const result = fibonachi(8); //21 
console.log(result); // 21
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Рекурсивные функции](https://metanit.com/web/javascript/3.4.php)
Iepriekšēja lapa >>> [[Funkcijas, kas pašas sevi izsauc]]
Nākama lapa >>> [[Navigācija JavaScript]]

---