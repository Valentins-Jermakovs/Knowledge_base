___

**Datums:** 2025-09-09
**Laiks:** 10:25
❚ **Tagi:** #javascript 

---
### Teksta virnknes kā īpašības un metodes

Vēl viens pieraksta veides ir teksta virkņu izmantošana:

```js
const user = {
    name: "Tom",
    age: 26,
    "full name": "Tom Johns",
    "display info": function(){
     
        console.log(user.name);
        console.log(user.age);
    }
};
console.log(user["full name"]);
user["display info"](); // metodes izsaukšana
user.display(); // metodes izsaukšana
```

Tā parocība ir tāda, kā var izmantot `space` īpašību un metožu nosaukumos.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объекты](https://metanit.com/web/javascript/4.1.php)
Iepriekšēja lapa >>> [[Masīvu sintakse]]
Nākama lapa >>> [[Dinamiska īpašību un metožu nosaukumu noteikšana]]

---