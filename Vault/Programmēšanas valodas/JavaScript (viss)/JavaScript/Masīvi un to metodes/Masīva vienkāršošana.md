___

**Datums:** 2025-08-15
**Laiks:** 12:15
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Metode `flat()`

Šī metode ļāuj vienkāršos masīvu, tas ir, ja masīvā ir citi masīvi, kas satur apakšmasīvus, tad to var pārveidot vienkārši par masīvu ar visu apakšmasīvu elementiem.

```js
const people = ["Tom", "Bob", ["Alice", "Kate", ["Sam", "Ann"]]];
const flattenPeople = people.flat();
console.log(flattenPeople); // ["Tom", "Bob", "Alice", "Kate", ["Sam", "Ann"]]
```

Kā parametru metode pieņem `dziļumu`, cik dziļi vienkāršot masīvu:

```js
const people = ["Tom", "Bob", ["Alice", "Kate", ["Sam", "Ann"]]];
const flattenPeople = people.flat(2);
console.log(flattenPeople); // ["Tom", "Bob", "Alice", "Kate", "Sam", "Ann"]
```

Ja mēs nezinām, cik dziļš ir šis masīvs, bet vēlamies to pilnībā vienkāršot, tad kā parametru nodod `Infinity`:

```js
const people = ["Tom", "Bob", ["Alice", "Kate", ["Sam", "Ann"]]];
const flattenPeople = people.flat(Infinity);
console.log(flattenPeople); // ["Tom", "Bob", "Alice", "Kate", "Sam", "Ann"]
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Операции с массивами](https://metanit.com/web/javascript/5.7.php)
Iepriekšēja lapa >>> [[Meklēšana masīvā]]
Nākama lapa >>> [[Elementu kārtības maiņa ar vecā masīva saglabāšanu]]

---