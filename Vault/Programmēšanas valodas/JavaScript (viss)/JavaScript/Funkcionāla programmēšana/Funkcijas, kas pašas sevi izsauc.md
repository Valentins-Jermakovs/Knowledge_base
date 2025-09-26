___

**Datums:** 2025-08-14
**Laiks:** 16:22
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Funkcijas, kas pašas sevi izsauc

Mēs varam izveidot funkciju, kas izsauks pati sevi:

```js
// самозывающаяся функция
(function(){
    console.log("Привет мир");
}());
```

Un šeit piemērs ar parametru nodošanu šādai funkcijai:

```js
(function (a, b){
      
    const result = a + b;
    console.log(`${a} + ${b} = ${result}`);
}(4, 5));
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Функции IIFE](https://metanit.com/web/javascript/3.13.php)
Iepriekšēja lapa >>> [[Bultu funkcijas (стрелочные функции)]]
Nākama lapa >>> [[Programmēšanas valodas/JavaScript (viss)/JavaScript/Funkcionāla programmēšana/Rekursīvas funkcijas]]

---