___

**Datums:** 2025-08-28
**Laiks:** 15:35
❚ **Tagi:** #javascript 

---
### Privātas metodes

Privātas metodes tiek izmantotas klases iekšējai loģikai un darbībai. Šajā piemēra pirms `name` iestatīšanas tiek veikta datu pārbaude:

```js
class Person{
    #name = "undefined";
    #age = 1;
    constructor(name, age){
        this.#name = this.#checkName(name);
        this.setAge(age);
    }
    #checkName(name){
        if(name!=="admin") return name;
    }
    setAge(age){
        if (age > 0 && age < 110) this.#age = age;
    }
    print(){
        console.log(`Name: ${this.#name}  Age: ${this.#age}`);
    }
}
const tom = new Person("Tom", 37);
tom.print();    // Name: Tom  Age: 37
const bob = new Person("admin", 41);
bob.print();    // Name: Undefined  Age 41
//let personName = bob.#checkName("admin"); // ! Ошибка - нельзя обратится к приватному методу
```

Kā arī parādīts, kas notiks, ja mēģināt piekļūt pie šādas privātas metodes.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Приватные поля и методы](https://metanit.com/web/javascript/4.16.php)
Iepriekšēja lapa >>> [[Privātie lauki]]
Nākama lapa >>> [[Navigācija - Privātie lauki un metodes]]

---