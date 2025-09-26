___

**Datums:** 2025-09-09
**Laiks:** 10:34
❚ **Tagi:** #javascript 

---
### Īpašību dzēšana

Objekta īpašību dzēšanai var izmantot šādas pieraksta formas:

```js
// punkta notācija
delete objekts.īpašība;

// masīvu sintakse
delete objekt["īpašība"];
```

Koda piemērs:

```js
let user = {};
user.name = "Tom";
user.age = 26;
user.display = function(){
     
    console.log(user.name);
    console.log(user.age);
};
 
console.log(user.name); // Tom
delete user.name; // удаляем свойство
// альтернативный вариант
// delete user["name"];
console.log(user.name); // undefined
```

Pēc īpašības dzēšanas tā būs `undefined`, tas nozīmē, kā tas vairs nav, un vēršanās pie izdzēstas īpašības atgriezīs kļūdu.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объекты](https://metanit.com/web/javascript/4.1.php)
Iepriekšēja lapa >>> [[Dinamiska īpašību un metožu nosaukumu noteikšana]]
Nākama lapa >>> [[Objekta izveide no mainīgiem un konstantēm]]

---