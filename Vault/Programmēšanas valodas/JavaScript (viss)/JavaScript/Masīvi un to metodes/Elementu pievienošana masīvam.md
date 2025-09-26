___

**Datums:** 2025-08-14
**Laiks:** 18:17
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Elementu pievienošana masīvam

##### push()

Metode `push()` pievieno elementu masīva beigās.

```js
const people = [];
people.push("Tom");
people.push("Sam");
people.push("Bob","Mike");
 
console.log("В массиве people элементов: ", people.length);
console.log(people); // ["Tom", "Sam", "Bob", "Mike"]
```
##### unshift()

Metode `unshift()` pievieno elementu masīva sākumā.

```js
const people = ["Bob"];
 
people.unshift("Alice");
console.log(people);    // ["Alice", "Bob"]
 
people.unshift("Tom", "Sam");
console.log(people);    // ["Tom", "Sam", "Alice", "Bob"]
```
##### Datu pievienošana pēc noteiktā indeksa

Metode `splice` ļauj pievienot elementus uz konkrētu indeksu. Metode pieņem 3 argumentus:

- `pirmais arguments` - indekss, pozīcija, uz kuru vajag ievietot jauno elementu;
- `otrais arguments` - elemntu skaits, ko bajag izdzēst. Šeit liec `0` nulli, jo elementus tu pievieno. Šī metode tiek izmantota arī dzēšanai;
- `trešais arguments/pārējie argumenti` - elementi, kas tiks pievienoti masīvam.

```js
const people = ["Tom", "Sam", "Bob"];
people.splice(1, 0, "Alice");  // добавляем элемент "Alice" по индексу 1
console.log(people);         // ["Tom", "Alice", "Sam", "Bob"]
```

```js
const people = ["Tom", "Sam", "Bob"];
people.splice(1, 0, "Alice", "Alex", "Kate");  // добавляем элемент "Alice" по индексу 1
console.log(people);         // ["Tom", "Alice", "Alex", "Kate", "Sam", "Bob"]
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Операции с массивами](https://metanit.com/web/javascript/5.7.php)
Iepriekšēja lapa >>> [[Operācijas ar masīviem (metodes)]]
Nākama lapa >>> [[Datu dzēšana no masīva]]

---