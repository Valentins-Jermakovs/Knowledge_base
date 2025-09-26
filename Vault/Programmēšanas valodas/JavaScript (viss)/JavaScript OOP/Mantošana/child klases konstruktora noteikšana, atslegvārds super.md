___

**Datums:** 2025-08-28
**Laiks:** 17:45
❚ **Tagi:** #javascript 

---
### `child` klases konstruktora noteikšana, atslegvārds `super`

`child` klasē arī var aprakstīt savu konstruktoru, taču pirms tam ir jānorāda `parent` klases konstruktoru, izmantojot atslēgvārdu `super`:

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
     
    constructor(name, age, company){
        super(name, age);
        this.company = company;
    }
    work(){
        console.log(`${this.name} works in ${this.company}`);
    }
}
  
const tom = new Person("Tom", 34);
tom.print();    // Name: Tom  Age: 34
 
const sam = new Employee("Sam", 25, "Google");
sam.print();    // Name: Sam  Age: 25
sam.work();     // Sam works in Google
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Наследование](https://metanit.com/web/javascript/4.15.php)
Iepriekšēja lapa >>> [[Klases mantošana ar konstruktoru]]
Nākama lapa >>> [[parent klases metožu pārdefinēšana child klasēs]]

---