___

**Datums:** 2025-08-28
**Laiks:** 17:40
❚ **Tagi:** #javascript 

---
### Klases mantošana ar konstruktoru

Kopā ar metodēm, `child` klase manto arī konstruktoru:

```js
class Person{
    constructor(name, age){
        this.name = name;
        this.age = age;
    }
    print(){
        console.log(`Name: ${this.name}  Age: ${this.age}`);
    }
}
class Employee extends Person{
    company;
    work(){
        console.log(`${this.name} works in ${this.company}`);
    }
}
  
const tom = new Person("Tom", 34);
tom.print();    // Name: Tom  Age: 34
 
const sam = new Employee("Sam", 25);    // унаследованный конструктор
sam.print();    // Name: Sam  Age: 25
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Наследование](https://metanit.com/web/javascript/4.15.php)
Iepriekšēja lapa >>> [[Ievads mantošanā]]
Nākama lapa >>> [[child klases konstruktora noteikšana, atslegvārds super]]

---