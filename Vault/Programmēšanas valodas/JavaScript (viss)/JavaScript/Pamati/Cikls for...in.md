___

**Datums:** 2025-08-13
**Laiks:** 19:14
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Cikls `for...in`

Šis cilks tiek izmantots, lai iterēt pa objekta vērtībām:

```js
const person = {name: "Tom", age: 37};
for(prop in person){
      
    console.log(prop);
}

// name
// age
```

```js
const person = {name: "Tom", age: 37};
for(prop in person){
      
    console.log(prop, person[prop]);
}
// name Tom
// age 37
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Циклы](https://metanit.com/web/javascript/2.7.php)
Iepriekšēja lapa >>> [[Cikls for...of]]
Nākama lapa >>> [[Programmēšanas valodas/JavaScript (viss)/JavaScript/Pamati/Cikls while]]

---