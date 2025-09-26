___

**Datums:** 2025-08-15
**Laiks:** 11:34
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Kārtošana pretējā virzienā

Šādai kārtošanai izmanto 2 metodes:

- `reverse()` - maina esošu sarakstu, kārto elementus pretējā virzienā;
- `toReversed()` - atgriež jaunu sarakstu, kas kārtots pretējā virzienā.

##### Metode `reverse()`

```js
const people = ["Tom", "Sam", "Bob"];
 
people.reverse();
console.log(people);         // ["Bob", "Sam", "Tom"]
```

##### Metode `toReversed()`

```js
const people = ["Tom", "Sam", "Bob"];
 
const reversed = people.toReversed();
console.log(people);         // ["Tom", "Sam", "Bob"]
console.log(reversed);         // ["Bob", "Sam", "Tom"]
```

*Piezīme. Šeit nav tādas īpatnības kā ar `sort()` un `toSorted()`.*

---
### ⇄ Saistības

Avots >>> [JavaScript \| Операции с массивами](https://metanit.com/web/javascript/5.7.php)
Iepriekšēja lapa >>> [[Kārtošana sort() un toSorted]]
Nākama lapa >>> [[Elementa indeksa meklēšana]]

---