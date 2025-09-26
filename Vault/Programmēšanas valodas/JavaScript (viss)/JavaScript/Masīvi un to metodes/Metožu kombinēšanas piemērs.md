___

**Datums:** 2025-08-15
**Laiks:** 12:33
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Metožu kombinēšana

Jā nepieciešams, var apvienot vairākas operācijas metožu ķēdē. Pieņemsim, kā mums ir lietotāju masīvs:

```js
function Person(name, age){
        this.name = name;
        this.age = age;
}
const people = [
        new Person("Tom", 38), new Person("Kate", 31), 
        new Person("Bob", 42), new Person("Alice", 34), 
        new Person("Sam", 25)
    ];
```

Tagad izvadīsim konsolē visus lietotāju vārdus, kuru vecums lielāks par 33:

```js
const isAgeMoreThan33 = (p)=>p.age > 33;
const getPersonName = (p)=>p.name;
const printPersonName = (p)=>console.log(p);
 // получаем из Person строку с именем
const view = people
                .filter(isAgeMoreThan33)
                .map(getPersonName)
                .forEach(printPersonName);
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Операции с массивами](https://metanit.com/web/javascript/5.7.php)
Iepriekšēja lapa >>> [[Masīva elementu apvienošana vienā vērtībā]]
Nākama lapa >>> [[Navigācija JavaScript]]

---