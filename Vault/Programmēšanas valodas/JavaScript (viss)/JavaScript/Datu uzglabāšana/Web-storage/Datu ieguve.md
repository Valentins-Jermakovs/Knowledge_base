___

**Datums:** 2025-08-30
**Laiks:** 14:22
❚ **Tagi:** #javascript 

---
### Datu ieguve

Lai iegūt datus, tiek izmantota metode `getItem()`, kurai tiek nodota atslēga `key`:

```js
// сохраняем в local storage
localStorage.setItem("email", "tom32@gmail.com");
// получаем обратно из local storage
const login = localStorage.getItem("email"); //tom32@gmail.com
```

Ja bija saglabāts skaitlis, tad nepieciešama tā konvertācija:

```js
localStorage.setItem("age", 23);
// преобразуем в число
let age = parseInt(localStorage.getItem("age"));
age += 1;
console.log(age); // 24
```

Ja bija saglabāts objekts, tad to vajag parsēt atpakaļ uz `JavaScript`:

```js
const tom ={
    name: "Tom",
    age: 23,
    isMarried: false
};
// konvertē uz JSON objektu un saglabā to krātuvē
localStorage.setItem("user", JSON.stringify(tom));
 
// преобразуем в объект
const user = JSON.parse(localStorage.getItem("user"));
console.log(user.name);  // Tom
console.log(user.age);  // 23
console.log(user.isMarried); // false
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Web Storage](https://metanit.com/web/javascript/12.2.php)
Iepriekšēja lapa >>> [[Datu saglabāšana]]
Nākama lapa >>> [[Dzēšana]]

---