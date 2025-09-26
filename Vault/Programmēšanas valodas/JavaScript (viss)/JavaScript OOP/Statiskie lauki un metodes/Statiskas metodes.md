___

**Datums:** 2025-08-28
**Laiks:** 16:16
❚ **Tagi:** #javascript 

---
### Statiskas metodes

Šīs metodes ir attiecināmas uz visu klasi. Šādam metodem ir aizliegta pieeja pie objekta laukiem pa taisno, izmantojot `this`. 

Pastāv vairākas atšķirības:

- `this` - tiek izmantots, lai piekļūt pie citiem statiskiem laukiem un metodēm;
- `static` - šis vārds definē statisko metodi;
- `static print(object)` - šādi tiek nodota piekļuve pie objekta laukiem, metodei tiek nodots pats objekts.

```js
class Person{
    static retirementAge = 65;
    constructor(name, age){
        this.name = name;
        this.age = age;
    }
    print(){ 
        console.log(`Имя: ${this.name}  Возраст: ${this.age}`);
    }
    static calculateRestAges(person){
        if(this.retirementAge > person.age){
            const restAges = this.retirementAge - person.age;
            console.log(`До пенсии осталось ${restAges} лет`);
        }
        else console.log("Вы уже на пенсии");
    }
}
const tom = new Person("Tom", 37);
Person.calculateRestAges(tom);      // До пенсии осталось 28 лет
const bob = new Person("Bob", 71);
Person.calculateRestAges(bob);      // Вы уже на пенсии
```

Kā redzam piemērā, pastāv statisks lauks `retirementAge` un statiska metode `calculateRestAges`. Metodei tiek nodots objekts un, lai piekļūt pie objekta laukiem, tiek rakstīts objekts un lauka nosaukums.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Статические поля и методы](https://metanit.com/web/javascript/4.17.php)
Iepriekšēja lapa >>> [[Statiskie lauki]]
Nākama lapa >>> [[Privātie statiskie lauki un metodes]]

---