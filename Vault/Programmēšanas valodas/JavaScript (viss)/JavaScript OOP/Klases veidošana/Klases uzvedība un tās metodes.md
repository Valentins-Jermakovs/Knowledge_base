___

**Datums:** 2025-08-28
**Laiks:** 15:02
❚ **Tagi:** #javascript 

---
### Klases uzvedība un tās metodes

Klases var saturēt arī metodes:

```js
class Person{
    name;
    age;
    move(place){
        console.log(`Go to ${place}`);
    }
    eat(){
        console.log("Eat apples");
    }
}
const tom = new Person();
tom.move("Hospital");   // Go to Hospital
tom.move("Cinema");     // Go to Cinema
tom.eat();              // Eat apples
```

Šeit klasē ir realizētas 2 metodes:

- `move()` - kas imitē cilvēka kustību;
- `eat()` - kas imitē ēšanas procesus.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Классы](https://metanit.com/web/javascript/4.12.php)
Iepriekšēja lapa >>> [[Klases lauki un īpašības]]
Nākama lapa >>> [[Vēršanās pie klases laukiem un metodem]]

---