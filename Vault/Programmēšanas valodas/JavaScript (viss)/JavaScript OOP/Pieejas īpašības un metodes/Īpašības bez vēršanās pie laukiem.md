___

**Datums:** 2025-08-28
**Laiks:** 15:57
❚ **Tagi:** #javascript 

---
### Īpašības bez vēršanās pie laukiem

Īpašības nav obligāti izmantot, lai piekļūt vai iestatīt laukus. Izmantojot īpašības var veidot arī parastas metodes, kas nav saistītas ar tiem:

```js
class Person{
    constructor(firstName, lastName){
        this.firstName = firstName;
        this.lastName = lastName;
    }
    get fullName(){ return `${this.firstName} ${this.lastName}` }
    set fullName(value){ 
        [this.firstName, this.lastName] = value.split(" ");
    }
}
const tom = new Person("Tom", "Smith");
console.log(tom.fullName);  // Tom Smith
tom.fullName = "Tomas Jefferson";
console.log(tom.lastName);  // Jefferson
```

Jā, šeit notiek dabība ar kalses laukiem, bet `fullName` metode atgriež jau nevis laukus, bet teksta rindu. 

---
### ⇄ Saistības

Avots >>> [JavaScript \| Свойства и методы доступа](https://metanit.com/web/javascript/4.14.php)
Iepriekšēja lapa >>> [[Īpašības tikai ierakstam]]
Nākama lapa >>> [[Navigācija - Pieejas īpašības un metodes]]

---