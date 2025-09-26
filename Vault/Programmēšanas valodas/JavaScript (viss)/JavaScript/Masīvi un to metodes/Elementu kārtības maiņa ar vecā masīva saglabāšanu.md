___

**Datums:** 2025-08-15
**Laiks:** 12:19
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Metode `with()`

Šī metode atgriež jauno masīvu un ļauj mainīt vecā masīvu elementus. Šī metode tiek izmantota, kad nepieciešams saglabāt vecā masīva kārtību.

```js
const people = ["Tom", "Bob", "Sam"];
const modified = people.with(0, "Tomas");   // изменяем "Tom" на "Tomas"
console.log(people);    // ["Tom", "Bob", "Sam"] - начальный массив не изменился
console.log(modified);  // ["Tomas", "Bob", "Sam"] - изменилась копия
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Операции с массивами](https://metanit.com/web/javascript/5.7.php)
Iepriekšēja lapa >>> [[Masīva vienkāršošana]]
Nākama lapa >>> [[Masīva elementu apvienošana vienā vērtībā]]

---