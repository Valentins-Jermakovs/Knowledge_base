___

**Datums:** 2025-08-14
**Laiks:** 15:45
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### `spread` operators

Obligāti `...{masīva_nosaukums}` 3 punkti, tas ir `spread` operators

```js
function printPerson(username, age, email) {
    console.log("Name:", username);
    console.log("Age:", age);
    console.log("Email:", email);
    console.log("=========================");
}
 
const tom = ["Tom", 39, "tom@example.com"]; 
const bob = ["Bob", 43, "bob@example.com"]; 
 
printPerson(...tom);
printPerson(...bob);
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Параметры функции](https://metanit.com/web/javascript/3.10.php)
Iepriekšēja lapa >>> [[Masīvs kā funkcijas parametrs]]
Nākama lapa >>> [[Neobligāti parametri, noklusējuma vērtības]]

---