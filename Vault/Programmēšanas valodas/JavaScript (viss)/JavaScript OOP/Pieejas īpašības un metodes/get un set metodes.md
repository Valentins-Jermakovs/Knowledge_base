___

**Datums:** 2025-08-28
**Laiks:** 15:45
❚ **Tagi:** #javascript 

---
### `get` un `set` metodes

Mēs varam izmantot vienu un to pašu metodi, gan lauka iestatīšanai, gan tā nolasīšanai:

```js
class Person{
    #ageValue = 1;
    constructor(name, age){
        this.name = name;
        this.age = age;
    }
    set age(value){
        console.log(`Передано ${value}`);
        if(value>0 && value < 110) this.#ageValue = value;
    }
    get age(){
        return this.#ageValue;
    }
}
const tom = new Person("Tom", 37);
console.log(tom.age);
tom.age = -15;
console.log(tom.age);
```

Šādas metodes izsaukšana ir tas pats, kā izsaukt publiskā tipa lauku.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Свойства и методы доступа](https://metanit.com/web/javascript/4.14.php)
Iepriekšēja lapa >>> [[Navigācija - Pieejas īpašības un metodes]]
Nākama lapa >>> [[Īpašības tikai lasīšana]]

---