___

**Datums:** 2025-08-28
**Laiks:** 16:24
❚ **Tagi:** #javascript 

---
### Privātie statiskie lauki un metodes

Tāpat kā parasti lauki un metodes, statiskie var būt arī kā privātie:

```js
class Person{
    static #retirementAge = 65;
    constructor(name, age){
        this.name = name;
        this.age = age;
    }
    print(){ 
        console.log(`Имя: ${this.name}  Возраст: ${this.age}`);
    }
    static calculateRestAges(person){
        if(this.#retirementAge > person.age){
            const restAges = this.#retirementAge - person.age;
            console.log(`До пенсии осталось ${restAges} лет`);
        }
        else console.log("Вы уже на пенсии");
    }
}
// console.log(Person.#retirementAge);  // ! Ошибка: поле retirementAge -приватное
const tom = new Person("Tom", 37);
Person.calculateRestAges(tom);      // До пенсии осталось 28 лет
const bob = new Person("Bob", 71);
Person.calculateRestAges(bob);      // Вы уже на пенсии
```

Šādi statiskie lauki un metodes var būt pieejami tikai pašā klasē.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Статические поля и методы](https://metanit.com/web/javascript/4.17.php)
Iepriekšēja lapa >>> [[Statiskas metodes]]
Nākama lapa >>> [[Navigācija - Statiskie lauki un metodes]]

---