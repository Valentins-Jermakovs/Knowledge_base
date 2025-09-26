___

**Datums:** 2025-08-28
**Laiks:** 17:33
❚ **Tagi:** #javascript 

---
### Ievads mantošanā

Mantošana ļauj samazināt koda apjomu `child` klasēs. Lai izveidot mantošanu, mums vajag `parent` klasi, `child` klasi un atslēgvārdu `extend`:

```js
class Base{}
class Derived extends Base{}
```

Sākumā iet `child` klase -> `extends` -> klase, kas tiek mantota `parent`.

```js
class Person{
    name;
    age;
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
  
const tom = new Person();
tom.name = "Tom"; 
tom.age= 34;
const bob = new Employee();
bob.name = "Bob"; 
bob.age = 36; 
bob.company = "Google";
tom.print();    // Name: Tom  Age: 34
bob.print();    // Name: Bob  Age: 36
bob.work();     // Bob works in Google
```

`child` klase manto `parent` klases konstruktora laukus un `parent` klases metodes. Tādejādi tiek samazināts koda apjoms.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Наследование](https://metanit.com/web/javascript/4.15.php)
Iepriekšēja lapa >>> [[Ievads mantošanā]]
Nākama lapa >>> [[Klases mantošana ar konstruktoru]]

---