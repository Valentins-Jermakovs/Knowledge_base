___

**Datums:** 2025-09-09
**Laiks:** 10:14
❚ **Tagi:** #javascript 

---
### Masīvu sintakse

Neskatoties uz to, cik tas mulsinoši skan, masīvi šeit n etiek izmantoti, tā vienk ārsi ir vēl viena papildus pieraksta forma objekta īpašību (lauku) veidošanai. Kā iepriekš, tiks izskatīti 2 veidi objekta inicializācijai.

Pakāpeniska:

```js
const user = {};
user["name"] = "Tom";
user["age"] = 26;
user["display"] = function(){ // šeit tiek veidota metode
     
    console.log(user.name);
    console.log(user.age);
};
 
// вызов метода
user["display"]();
```

Uzreiz:

```js
const user = {
    ["name"]: "Tom",
    ["age"]: 26,
    ["display"]: function(){  // šeit tiek veidota metode
      
        console.log(user.name);
        console.log(user.age);
    }
};
user["display"]();
```

Kā redzams, lai piekļūt pie objekta īpašībām un metodem, var izmantot gan punktu: `user.display()`, gan masīvu pierakstu: `user["display"]();`.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объекты](https://metanit.com/web/javascript/4.1.php)
Iepriekšēja lapa >>> [[Objekta metodes]]
Nākama lapa >>> [[Teksta virnknes kā īpašības un metodes]]

---