___

**Datums:** 2025-08-14
**Laiks:** 18:02
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Masīvu kopēšana

Operators `spread` ļauj gana vienkārši kopēt masīvu.

```js
const people = ["Sam", "Tom", "Bob"];
const employees = [...people];
employees[0] = "Dan";
console.log(employees);     // ["Dan", "Tom", "Bob"]
console.log(people);        //  ["Sam", "Tom", "Bob"]
```

*Piezīme. Šeit masīvs ir konstante. Konstante aizliedz pārrakstīt, ja konstante ir masīvs, tad mums ir atļauts mainīt masīvu, uz kuru atsaucas konstante.*

---
### ⇄ Saistības

Avots >>> [JavaScript \| Массивы и spread-оператор](https://metanit.com/web/javascript/5.6.php)
Iepriekšēja lapa >>> [[Masīva nodošana funkcijai]]
Nākama lapa >>> [[Operācijas ar masīviem (metodes)]]

---