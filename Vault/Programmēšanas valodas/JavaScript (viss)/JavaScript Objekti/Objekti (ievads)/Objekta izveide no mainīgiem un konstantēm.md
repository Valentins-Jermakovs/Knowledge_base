___

**Datums:** 2025-09-09
**Laiks:** 10:42
❚ **Tagi:** #javascript 

---
### Objekta izveide no mainīgiem un konstantēm

Objekta īpašību inicializācijai mēs varam izmantot mainīgos un konstantes:

```js
function getSalary(status){
    if(status==="senior") return 1500;
    else return 500;
}
const name = "Tom";
const age = 37;
const person = { name: name, age: age, salary: getSalary()};
 
console.log(person);    // {name: "Tom", age: 37, salary: 500}
```

Taču, ja mainīgo/konstanšu nosaukumi sakrīt ar īpašību nosaukumiem, var izmantot šādu pieraksta formu:

```js
const name = "Tom";
const age = 37;
const salary = 500;
const person = { name, age, salary};
 
console.log(person);    // {name: "Tom", age: 37, salary: 500}
```

Tas pats tiek attiecināts pie parametru nodošansa funkcijām:

```js
function display(){ 
    console.log(this.name, this.age);
}
const move = function(place){ console.log(this.name, "goes to", place)};
const name = "Tom";
const age = 37;
const salary = 500;
const person = { name, age, salary, display, move};
 
person.display();       // Tom 37
person.move("cinema");  // Tom goes to cinema
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объекты](https://metanit.com/web/javascript/4.1.php)
Iepriekšēja lapa >>> [[Īpašību dzēšana]]
Nākama lapa >>> [[Funkcija Object.fromEntries()]]

---