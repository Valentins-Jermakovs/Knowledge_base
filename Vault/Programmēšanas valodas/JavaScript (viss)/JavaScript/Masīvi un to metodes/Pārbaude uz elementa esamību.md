___

**Datums:** 2025-08-15
**Laiks:** 11:42
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Pārbaude uz elementa esamību

Metode `includes()` ļauj pārbaudīt, vai masīvā eksistē meklējamais elements. Ja tāds ir, atgriež `True`, pretējā gadījumā `False`.

```js
const people = ["Tom", "Sam", "Bob", "Tom", "Alice", "Sam"];
 
console.log(people.includes("Tom"));    // true - Tom есть в массиве
console.log(people.includes("Kate"))    // false - Kate нет в массиве
```

Otrais  metodes parametrs ir indekss, no kura sāk meklēšanu:

```js
const people = ["Tom", "Sam", "Bob", "Tom", "Alice", "Sam"];
 
console.log(people.includes("Bob", 2)); // true
console.log(people.includes("Bob", 4))  // false
```

Var norādīt arī negatīvu skaitli, jeb pēdējo elementu, no kura ies meklēšana līdz masīva beigām:

```js
const people = ["Tom", "Sam", "Bob", "Tom", "Alice", "Sam"];
 
console.log(people.includes("Tom", -2)); // false - 2-й индекс с конца
console.log(people.includes("Tom", -3)) // true - 3-й индекс с конца
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Операции с массивами](https://metanit.com/web/javascript/5.7.php)
Iepriekšēja lapa >>> [[Elementa indeksa meklēšana]]
Nākama lapa >>> [[Masīva elementu pārbaude uz nosacījumu]]

---