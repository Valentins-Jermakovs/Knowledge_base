___

**Datums:** 2025-09-09
**Laiks:** 10:47
❚ **Tagi:** #javascript 

---
### Funkcija `Object.fromEntries()`

Izmantojot funkciju `Object.fromEntries()` var veidot objektu no `key-value` pāriem. Šeit piemērs ar masīvu:

```js
const personData = [ ["name", "Tom"], ["age", 37]];
const person = Object.fromEntries(personData);
console.log(person);        // {name: "Tom", age: 37}
console.log(person.name);    // Tom
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объекты](https://metanit.com/web/javascript/4.1.php)
Iepriekšēja lapa >>> [[Objekta izveide no mainīgiem un konstantēm]]
Nākama lapa >>> [[Navigācija - JavaScript Objekti]]

---