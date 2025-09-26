___

**Datums:** 2025-08-28
**Laiks:** 15:11
❚ **Tagi:** #javascript 

---
### Konstruktora noteikšana

Lai izveidot objektu klasei, tiek izmantots konstruktors:

```js
const bob = new Person();
```

Tas ir noklusējuma konstruktors, kas tiek izmantots visbiežāk, taču mēs varam izmantot konstruktoru arī pašās klasēs.

```js
class Person{
    name;
    age;
    constructor(){
        console.log("Вызов конструктора");
    }
    print(){
        console.log(`Name: ${this.name}  Age: ${this.age}`);
    }
}
const tom = new Person();   // Вызов конструктора
const bob = new Person();   // Вызов конструктора
```

Šāds iekšējs konstruktors parasti tiek izmantots, lai inicianalizēt objektu ar sākuma datiem:

```js
class Person{
    name;
    age;
    constructor(pName, pAge){
        this.name = pName;
        this.age = pAge;
    }
    print(){
        console.log(`Name: ${this.name}  Age: ${this.age}`);
    }
}
const tom = new Person("Tom", 37);
tom.print();    // Name: Tom  Age: 37
const bob = new Person("Bob", 41); 
bob.print()     // Name: Bob  Age: 41
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Классы](https://metanit.com/web/javascript/4.12.php)
Iepriekšēja lapa >>> [[Vēršanās pie klases laukiem un metodem]]
Nākama lapa >>> [[Navigācija - Klases veidošana]]

---