___

**Datums:** 2025-08-14
**Laiks:** 17:49
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### `spread` operators

Šis operators  ļauj izjaukt masīvu uz elementiem.

Sintakse:

```js
...masīva_nosaukums
```

Parasts piemērs:

```js
const users = ["Tom", "Sam", "Bob"];
console.log(...users);  // Tom Sam Bob
```

Izmantojot šo operatoru mēs varam izvilkt elementus no viena masīva un ierakstīt tos citā:

```js
const users = ["Tom", "Sam", "Bob"];
console.log(users);     //  ["Tom", "Sam", "Bob"]
const people1 = [...users];
const people2 = new Array(...users);
const people3 = Array.of(...users);
console.log(people1);     //  ["Tom", "Sam", "Bob"]
console.log(people2);     //  ["Tom", "Sam", "Bob"]
console.log(people3);     //  ["Tom", "Sam", "Bob"]
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Массивы и spread-оператор](https://metanit.com/web/javascript/5.6.php)
Iepriekšēja lapa >>> [[length metode]]
Nākama lapa >>> [[Masīvu apvienošana]]

---