___

**Datums:** 2025-08-15
**Laiks:** 12:06
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Meklēšana masīvā

Meklēšanai tiek izmantotas 4 metodes:

- `find()` - atgriež pirmo elementu, kas atbilst nosacījumam;
- `findLast()` - atgriež pēdējo elementu, kas atbilst nosacījumam;
- `findIndex()` - atgriež indeksu pirmai sakritībai, kas atbilst nosacījuma;
- `findLastIndex()` - atgriež indeksu pēdējai sakritībai, kas atbilst nosacījumam.

Visas metodes kā parametru saņem funkciju. uz kuru tiek veikta pārbaude.

##### Metode `find()`

```js
const numbers = [1, 2, 3, 5, 8, 13, 21, 34];
 
// получаем первый элемент, который больше 10
let found = numbers.find(n => n > 10 );
console.log(found); // 13
```

##### Metode `findLast()`

```js
const numbers = [1, 2, 3, 5, 8, 13, 21, 34];
 
// получаем последний элемент, который меньше 10
let found = numbers.find(n => n < 10 );
console.log(found); // 8
```

##### Metode `findIndex()`

```js
const numbers = [1, 2, 3, 5, 8, 13, 21, 34];
 
// получаем индекс первого элемента, который больше 10
let foundIndex = numbers.findIndex(n => n > 10 );
console.log(foundIndex);    // 5
```

##### Metode `findLastIndex()`

```js
const numbers = [1, 2, 3, 5, 8, 13, 21, 34];
 
// получаем индекс последнего элемента,  который меньше 10
let foundIndex = numbers.findIndex(n => n < 10 );
console.log(foundIndex);    // 4
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Операции с массивами](https://metanit.com/web/javascript/5.7.php)
Iepriekšēja lapa >>> [[Masīva transformācija]]
Nākama lapa >>> [[Masīva vienkāršošana]]

---