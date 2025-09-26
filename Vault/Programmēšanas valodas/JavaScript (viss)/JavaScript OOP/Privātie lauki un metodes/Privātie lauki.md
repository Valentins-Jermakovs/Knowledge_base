___

**Datums:** 2025-08-28
**Laiks:** 15:29
❚ **Tagi:** #javascript 

---
### Privātie lauki

Iepriekšējās nodaļās tika izmantoti publiskie lauki, kas pieejami jebkurā programmas daļā. Lai pasargāt datus un padarīt programmu stabilu, tiek izmantoti privātie lauki. Tie aizliedz datu maiņu. Lai izveidot privātus laukus, izmanto `#` simbolu.

Šajā piemērā parādīts, kā veidot šādus laukus un kas būs, ja mēģinās mainīt privātos objekta datus:

```js
class Person{
    #name;
    #age;
    constructor(name, age){
        this.#name = name;
        this.#age = age;
    }
    print(){
        console.log(`Name: ${this.#name}  Age: ${this.#age}`);
    }
}
const tom = new Person("Tom", 37);
// tom.#name = "Sam";   // ! Ошибка - нельзя обратиться к приватному полю
// tom.#age = -45;      // ! Ошибка - нельзя обратиться к приватному полю
tom.print();    // Name: Tom  Age: 37
```

Nākamajā piemērā parādīts, kā caur klases metodem var pārrakstīt privātos laukus:

```js
class Person{
    #name;
    #age = 1;
    constructor(name, age){
        this.#name = name;
        this.setAge(age);
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
tom.setAge(22);
tom.print();    // Name: Tom  Age: 22
tom.setAge(-1234);
tom.print();    // Name: Tom  Age: 22
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Приватные поля и методы](https://metanit.com/web/javascript/4.16.php)
Iepriekšēja lapa >>> [[Navigācija - Privātie lauki un metodes]]
Nākama lapa >>> [[Privātas metodes]]

---