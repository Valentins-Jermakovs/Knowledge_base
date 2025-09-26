___

**Datums:** 2025-08-14
**Laiks:** 18:19
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Datu dzēšana

##### pop()

Metode `pop()` izvelk un dzēš pēdējo elementu no masīva.

```js
const people = ["Tom", "Sam", "Bob", "Mike"];
 
const lastPerson = people.pop(); // извлекаем из массива последний элемент
console.log(lastPerson );   // Mike
console.log(people);    // ["Tom", "Sam", "Bob"]
```
##### shift()

Metode `shift()` izvelk un dzēš pirmo elementu no masīva.

```js
const people = ["Tom", "Sam", "Bob", "Mike"];
 
const first = people.shift(); // извлекаем из массива первый элемент
console.log(first); // Tom
console.log(people);    // ["Sam", "Bob", "Mike"]
```
##### Elementa dzēšana pēc indeksa splice()

Metode `splice` tiek izmantota ne tikai elementu pievienošanai, bet arī dzēšanai.

```js
const people = ["Tom", "Sam", "Bill", "Alice", "Kate"];
const deleted = people.splice(3);
console.log(deleted);        // [ "Alice", "Kate" ]
console.log(people);         // [ "Tom", "Sam", "Bill" ]
```

Šeit tiek izdēsti pirmie 3 elementi. Metode atgriež izdzēstos elementus kā masīvu.
Ja norādīt negatīvu skaitli, tad tiks dzēsti masīva pēdējie elementi:

```js
const people = ["Tom", "Sam", "Bill", "Alice", "Kate"];
const deleted = people.splice(-1);
console.log(deleted);       // [ "Kate" ]
console.log(people);        // ["Tom", "Sam", "Bill", "Alice"]
```

Papildus var norādīt sākuma un beigu indeksus:

```js
const people = ["Tom", "Sam", "Bill", "Alice", "Kate"];
const deleted = people.splice(1, 3);
console.log(deleted);        // ["Sam", "Bill", "Alice"]
console.log(people);         // ["Tom", "Kate"]
```
##### Elementu maiņa

Mēs varam kombinēt gan elementu pievienošanu, gan to dzēšanu.

```js
const people = ["Tom", "Sam", "Bob", "Alice", "Kate"];
const deleted = people.splice(1, 3, "Alex", "Mike");
console.log(deleted);        // ["Sam", "Bob", "Alice"]
console.log(people);         // ["Tom", "Alex", "Mike", "Kate"]
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Операции с массивами](https://metanit.com/web/javascript/5.7.php)
Iepriekšēja lapa >>> [[Elementu pievienošana masīvam]]
Nākama lapa >>> [[Masīvu kopēšana (padziļināti)]]

---