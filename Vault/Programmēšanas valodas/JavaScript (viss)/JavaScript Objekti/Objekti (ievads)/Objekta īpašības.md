___

**Datums:** 2025-09-09
**Laiks:** 10:02
❚ **Tagi:** #javascript 

---
### Objekta īpašības

Objekta īpašību noteikšanai tiek izmantotas dažādas pieejas:

- Standarta un mūsdienāš biežāk izmantota pieeja ir noteikt īpašības objekta izveidošanas laikā:

```js
const user = {
    name: "Tom",
    age: 26
};
```

- Otrs veids ir šākumā izveidot objektu un tad pakāpeniski pievienot tam īpašības:

```js
// pirmais veids
const user = {};
user.name = "Tom";
user.age = 26;

// otrs veids - mainīgie
const name = "Tom";
const age = 34;
const user = {name, age};
console.log(user.name);     // Tom
console.log(user.age);      // 34

// Otrajā gadījumā mainīgie ir objekta lauku nosaukumi

const name = "Tom";
const age = 34;
const user = {name, age};
 
const teacher = {user, course: "JavaScript"};
console.log(teacher.user);      // {name: "Tom", age: 34}
console.log(teacher.course);    // JavaScript
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объекты](https://metanit.com/web/javascript/4.1.php)
Iepriekšēja lapa >>> [[Objekta izveide]]
Nākama lapa >>> [[Objekta metodes]]

---