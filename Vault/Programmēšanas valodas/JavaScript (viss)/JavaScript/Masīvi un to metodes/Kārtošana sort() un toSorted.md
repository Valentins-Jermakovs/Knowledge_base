___

**Datums:** 2025-08-15
**Laiks:** 11:01
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Kārtošana

Masīva kārtošanai tiek izmantotas šāds metode:

- `sort()` - maina esošo masīvu;
- `toSorted` - atgriež jauno, sakārtotot masīvu.

*Piezīme. Abas metodes kārto alfabēta secībā, kas var novest pie negaidītiem rezultātiem.*

##### Metode `sort()`

Metode kārto masīvu augošā secībā, pēc alfabēta.

```js
const people = ["Tom", "Sam", "Bob"];
 
people.sort();
console.log(people);         // ["Bob", "Sam", "Tom"]
```

Šī metode apsakta masīva elementus kā teksta virkni, kas var novest pie negaidīta rezultāta:

```js
const numbers = [200, 15, 5, 35];
 
numbers.sort();
console.log(numbers);         // [15, 200, 35, 5]
```

Lai izvairītos no tādam situācijām, nodod metodei kārtošanas funkciju:

```js
const numbers = [200, 15, 5, 35];
 
numbers.sort( (a, b) =>  a - b);
console.log(numbers);         // [5, 15, 35, 200]
```

##### Metode `toSorted`

Tas pats kā iepriekšēja metode, bet atgriež kārtoto masīvu.

Tā pati lieta ar šķirošanu pēc alfabēta:

```js
const numbers = [200, 15, 5, 35];
 
const sorted = numbers.toSorted();
console.log(sorted);         // [15, 200, 35, 5]
```

Lai šo lietu izlabot, nodod šķirošanas funkciju:

```js
const numbers = [200, 15, 5, 35];
const sorted = numbers.toSorted( (a, b) =>  a - b);
console.log(sorted);         // [5, 15, 35, 200]
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Операции с массивами](https://metanit.com/web/javascript/5.7.php)
Iepriekšēja lapa >>> [[Metode join()]]
Nākama lapa >>> [[Kārtošana pretējā virzienā]]

---