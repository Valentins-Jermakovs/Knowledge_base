___

**Datums:** 2025-08-13
**Laiks:** 18:42
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Masīva izveide

Kā jebkurā valodā, elementu indeksācija sākas no `0` nulles. Lai izveidot masīvu, izmanot `[]`.

```js
const myArray = []; // tukšais masīvs

const people = ["Tom", "Alice", "Sam"];
console.log(people);    // ["Tom", "Alice", "Sam"];
```

Piekļuve pie masīva elementiem un to modifikācija:

```js
const people = ["Tom", "Alice", "Sam"];
console.log(people[0]); // Tom
people[0] = "Bob";
console.log(people[0]); // Bob
```

`JavaScript` valodā masīvi nav stingri tipizēti, tas nozīmē, kā tie var glabāt dažādus datus.

```js
const objects = ["Tom", 12, true, 3.14, false];
console.log(objects);
```
##### 2D masīvi

```js
const numbers2 = [[0, 1, 2], [3, 4, 5]]; // двумерный массив

const people = [
    ["Tom", 25, false],
    ["Bill", 38, true],
    ["Alice", 21, false]
];
 
console.log(people[0]); // ["Tom", 25, false]
console.log(people[1]); // ["Bill", 38, true]

console.log("Имя: ", people[0][0]); // Tom
console.log("Возраст: ", people[0][1]); // 25
```

Elementu modifikācija:

```js
const people = [
    ["Tom", 25, false],
    ["Bill", 38, true],
    ["Alice", 21, false]
];
people[0][1] = 56; // присваиваем отдельное значение
console.log(people[0][1]); // 56
     
people[1] = ["Bob", 29, false]; // присваиваем массив
console.log(people[1][0]); // Bob
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Введение в массивы](https://metanit.com/web/javascript/2.5.php)
Iepriekšēja lapa >>> [[Programmēšanas valodas/JavaScript (viss)/JavaScript/Pamati/Datu konvertācija|Datu konvertācija]]
Nākama lapa >>> [[Nosacījuma konstrukcijas]]

---