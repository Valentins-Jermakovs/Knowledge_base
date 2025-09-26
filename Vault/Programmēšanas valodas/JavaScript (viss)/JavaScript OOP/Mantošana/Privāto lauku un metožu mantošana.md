___

**Datums:** 2025-08-28
**Laiks:** 17:52
❚ **Tagi:** #javascript 

---
### Privāto lauku un metožu mantošana

Mantošanai ir viena īpatnība, `child` klases nevar mantot privātus laukus un metodes:

```js
class Person{
    #name;
    constructor(name, age){
        this.#name = name;
        this.age = age;
    }
    print(){
        console.log(`Name: ${this.#name}  Age: ${this.age}`);
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
    work(){
        console.log(`${this.#name} works in ${this.company}`);  // ! Ошибка - поле #name недоступно из Employee
    }
}
```

Lai varētu piekļūt privātiem datiem, `parent` klasē nosaki *getterus un setterus*, kas vēršas pie privātiem laukiem un jau `child` klasē šie *getteri un setteri* ļaus piekļūt pie `parent` klases laukiem.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Наследование](https://metanit.com/web/javascript/4.15.php)
Iepriekšēja lapa >>> [[parent klases metožu pārdefinēšana child klasēs]]
Nākama lapa >>> [[Navigācija - Mantošana]]

---