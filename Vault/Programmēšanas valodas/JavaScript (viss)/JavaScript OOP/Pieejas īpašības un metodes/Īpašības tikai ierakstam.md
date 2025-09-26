___

**Datums:** 2025-08-28
**Laiks:** 15:52
❚ **Tagi:** #javascript 

---
### Īpašības tikai ierakstam

Tas pats, kas iepriekš, bet tikai datu ieraksts, īpašība `set`:

```js
class Person{
    #id;
    constructor(name, age, id){
        this.name = name;
        this.age = age;
        this.id = id;
    }
    set id(value){ this.#id = value;}
    print(){
        console.log(`id: ${this.#id}   name: ${this.name}   age: ${this.age}`);
    }
}
const tom = new Person("Tom", 37, 1);
tom.print();            // id: 1   name: Tom   age: 37
tom.id = 55;            // устанавливаем значение свойства id
tom.print();            // id: 55   name: Tom   age: 37
console.log(tom.id);    // undefined - значение свойства id нельзя получить
```

Kā redzam, metode `id()` ļauj veikt tikai datu ierakstu.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Свойства и методы доступа](https://metanit.com/web/javascript/4.14.php)
Iepriekšēja lapa >>> [[Īpašības tikai lasīšana]]
Nākama lapa >>> [[Īpašības bez vēršanās pie laukiem]]

---