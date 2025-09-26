___

**Datums:** 2025-08-28
**Laiks:** 15:49
❚ **Tagi:** #javascript 

---
### Īpašības tikai lasīšana

Iepriekšējā rakstā tika izmantots gan `set`, gan `get`. Taču mums nav obligāti izmantot abas šādas īpašības. Piemēram, mēs varam izveidot metodi, kas tiks izmantota tikai datu nolasīšanai:

```js
class Person{
    #age = 1;
    #name;
    constructor(name, age){
        this.#name = name;
        this.age = age;
    }
    //set name(value){ this.#name = value; }
    get name(){ return this.#name; }
    set age(value){ if(value>0 && value < 110) this.#age = value; }
    get age(){ return this.#age; }
}
const tom = new Person("Tom", 37);
console.log(tom.name);  // Tom
tom.name = "Bob";       // Это ничего не даст
console.log(tom.name);  // Tom   - значение не изменилось
```

Kā redzams, metode `name()` ļauj mums tikai nolasīt privāto lauku.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Свойства и методы доступа](https://metanit.com/web/javascript/4.14.php)
Iepriekšēja lapa >>> [[get un set metodes]]
Nākama lapa >>> [[Īpašības tikai ierakstam]]

---