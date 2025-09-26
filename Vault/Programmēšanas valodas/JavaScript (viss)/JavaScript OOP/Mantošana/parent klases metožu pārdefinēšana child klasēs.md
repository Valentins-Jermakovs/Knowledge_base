___

**Datums:** 2025-08-28
**Laiks:** 17:49
❚ **Tagi:** #javascript 

---
### `parent` klases metožu pārdefinēšana `child` klasēs

Ja mums vajag pārdefinēt, pārrakstīt kādu no `parent` klases metodēm `child` klasē, mēs definējam jauno klasi ar identisko nosaukumu. Taču ja mēs vēlamies papildināt `parent` klases metodi, tad izmantojam atslēgvārdu `super`:

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
    print(){
        super.print();
        console.log(`Company: ${this.company}`);
    }
}
const sam = new Employee("Sam", 25, "Google");
sam.print();    // Name: Sam  Age: 25
                // Company: Google
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Наследование](https://metanit.com/web/javascript/4.15.php)
Iepriekšēja lapa >>> [[child klases konstruktora noteikšana, atslegvārds super]]
Nākama lapa >>> [[Privāto lauku un metožu mantošana]]

---