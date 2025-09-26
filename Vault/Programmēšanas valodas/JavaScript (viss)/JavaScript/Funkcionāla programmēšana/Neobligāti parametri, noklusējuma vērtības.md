___

**Datums:** 2025-08-14
**Laiks:** 15:50
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Neobligāti parametri

Funkcijai var iestatīt parametru noklusējuma vērtības.

```js
function sum(x = 8, y = 5){
 
    const z = x + y;
    console.log(z);
}
sum();      // 13
sum(6);     // 11
sum(6, 4)   // 10
```

Var darīt pat šādi:

```js
function sum(x = 8, y = 10 + x){
 
    const z = x + y;
    console.log(z);
}
sum();      // 26
sum(6);     // 22
sum(6, 4)   // 10
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Параметры функции](https://metanit.com/web/javascript/3.10.php)
Iepriekšēja lapa >>> [[spread operators]]
Nākama lapa >>> [[Funkcijas kā parametri]]

---