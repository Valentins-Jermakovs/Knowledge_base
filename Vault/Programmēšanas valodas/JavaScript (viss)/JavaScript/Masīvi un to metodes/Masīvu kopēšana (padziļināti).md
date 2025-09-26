___

**Datums:** 2025-08-14
**Laiks:** 18:35
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Kopēšana

Pastāv vairāki veidi, kā kopēt masīvus.

##### Nedziļa kopēšana

Šajā variantā 2 mainīgie atsaucas uz vienu un to pašu masīvu.

```js
const users = ["Tom", "Sam", "Bill"];
console.log(users);     //  ["Tom", "Sam", "Bill"]
const people = users;   //  неглубокое копирование
 
people[1] = "Mike";     //  изменяем второй элемент
console.log(users);     //  ["Tom", "Mike", "Bill"]
```

##### Operators `spread`

Vienkāršs veids, kā kopēt visu masīvu:

```js
const users = ["Tom", "Sam", "Bill"];
console.log(users);     //  ["Tom", "Sam", "Bill"]
const people = [...users];
  
people[1] = "Mike";     //  изменяем второй элемент
console.log(users);     //  ["Tom", "Sam", "Bill"]
console.log(people);     //  ["Tom", "Mike", "Bill"]
```

##### Metode `slice()`

Vienkāršs veids, kā kopēt visu masīvu:

```js
const users = ["Tom", "Sam", "Bill"];
console.log(users);             //  ["Tom", "Sam", "Bill"]
const people = users.slice();       //  глубокое копирование
 
people[1] = "Mike";             //  изменяем второй элемент
console.log(users);             //  ["Tom", "Sam", "Bill"]
console.log(people);            //  ["Tom", "Mike", "Bill"]
```

Šī metode ļauj kopēt arī kādu daļu no masīva:

```js
slice(sākuma_indekss, beigu_indekss)
```

```js
const users = ["Tom", "Sam", "Bill", "Alice", "Kate"];
const people = users.slice(2);  // со второго индекса до конца
console.log(people);        // ["Bill", "Alice", "Kate"]
```

```js
const users = ["Tom", "Sam", "Bill", "Alice", "Kate"];
const people = users.slice(-2);  // до второго индекса с конца
console.log(people);        // ["Alice", "Kate"]
```

```js
const users = ["Tom", "Sam", "Bill", "Alice", "Kate"];
const people = users.slice(1, 4);
console.log(people);        // ["Sam", "Bill", "Alice"]
```

```js
const users = ["Tom", "Sam", "Bill", "Alice", "Kate"];
const people = users.slice(2, -1);  // с индекса 2 по индекс 1 с конца
console.log(people);        // ["Bill", "Alice"]
```

##### Metode `copyWithin()`

Metode pieņem trīs parametrus:

```js
copyWithin(index1, index2, index3)
```

- `index1` - pozīcija, kur tiks ievietoti kopējamie elementi;
- `index2` - sākuma pozīcija, no kuras tiks kopēti elementi;
- `index3` - beigu pozīcija, līdz kurai tiks kopēti elementi.

```js
const users = ["Tom", "Sam", "Bob", "Alice", "Kate"];
const people = users.copyWithin(1, 3, 5);  // элементы с индекса 3 по индекс 4 (два элемента)
                                            // копируются по индексу 1
console.log(people);    // ["Tom", "Alice", "Kate", "Alice", "Kate"]
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Операции с массивами](https://metanit.com/web/javascript/5.7.php)
Iepriekšēja lapa >>> [[Datu dzēšana no masīva]]
Nākama lapa >>> [[Elementu iegūšana ārpus diapazona]]

---