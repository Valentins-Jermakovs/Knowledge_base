___

**Datums:** 2025-08-14
**Laiks:** 17:00
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Masīva izveide

Pastāv vairāķi veidi, kā var izveidot masīvu.

Pirmais veids, konstruktors un `[]` kvadrātiekavas:

```js
const users = new Array();
const people = [];
 
console.log(users); // Array[0]
console.log(people); // Array[0]
```

Var veikt inicializāciju ar elementiem:

```js
const users = new Array("Tom", "Bill", "Alice");
const people = ["Sam", "John", "Kate"];
 
console.log(users); // ["Tom", "Bill", "Alice"]
console.log(people); // ["Sam", "John", "Kate"]
```

Var pievienot elementus, norādot to indeksus:

```js
const users = [];
users[1] = "Tom";
users[2] = "Kate";
console.log(users[1]); // "Tom"
console.log(users[0]); // undefined
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Создание массива и объект Array](https://metanit.com/web/javascript/5.3.php)
Iepriekšēja lapa >>> [[Navigācija JavaScript]]
Nākama lapa >>> [[Metode Array.from]]

---