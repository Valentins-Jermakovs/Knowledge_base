___

**Datums:** 2025-08-28
**Laiks:** 15:07
❚ **Tagi:** #javascript 

---
### Vēršanās pie klases laukiem un metodem

Ja mēs vēlamies vērsties pie klases laukiem un metodēm, tiek izmantots vārds `this`:

```js
class Person{
    name;
    age;
    print(){
        console.log(`Name: ${this.name}  Age: ${this.age}`);
    }
}
const tom = new Person();
tom.name = "Tom";
tom.age = 37;
tom.print();    // Name: Tom  Age: 37
 
const bob = new Person();
bob.name = "Bob";
bob.age = 41;
bob.print();    // Name: Bob  Age: 41
```

Tas ļauj izmantot klases laukus un metodes. Piemērā klases lauki tiek nodoti tās metodei `print()`.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Классы](https://metanit.com/web/javascript/4.12.php)
Iepriekšēja lapa >>> [[Klases uzvedība un tās metodes]]
Nākama lapa >>> [[Konstruktora noteikšana]]

---