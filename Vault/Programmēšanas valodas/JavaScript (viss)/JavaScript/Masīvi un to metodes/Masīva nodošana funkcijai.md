___

**Datums:** 2025-08-14
**Laiks:** 17:54
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Masīva nodošana funkcijai

Izmantojot `spread` operatoru, var nodot masīva elementus funkcijai.

```js
const people1 = ["Tom", "Sam", "Bob", "Mike"];
const people2 = ["Alex", "Bill"];
function print(first, second, third){
    console.log(`${first}, ${second}, ${third}`);
}
print(...people1);  // Tom, Sam, Bob
print(...people2);  // Alex, Bill, undefined
```

Šeit `undefined`, jo pēdējā masīvā ir tikai 2 elementi.

```js
const people = ["Tom", "Sam", "Bob"];
 
function print(first, second, third){
    console.log(first);
    console.log(second);
    console.log(third);
}
print(...people); 
// Tom
// Sam
// Bob
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Массивы и spread-оператор](https://metanit.com/web/javascript/5.6.php)
Iepriekšēja lapa >>> [[Masīvu apvienošana]]
Nākama lapa >>> [[Masīvu kopēšana]]

---