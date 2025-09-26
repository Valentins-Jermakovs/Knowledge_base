___

**Datums:** 2025-08-28
**Laiks:** 16:09
❚ **Tagi:** #javascript 

---
### Statiskie lauki

Tie ir kā tādi kopēji, vispārēji klasei raksturīgie dati. Šādi dati būsvienādi visiem klases objektiem. To definēšanai izmanto `static`. Lai pie šādiem datiem piekļūt, vajag norādīt klases nosaukumu un statiskā lauka nosaukumu.

```js
class Person{
    static retirementAge = 65;
    constructor(name, age){
        this.name = name;
        this.age = age;
    }
    print(){ 
        console.log(`Имя: ${this.name}  Возраст: ${this.age}`); 
    }
}
 
console.log(Person.retirementAge); // 65
Person.retirementAge = 62;
console.log(Person.retirementAge); // 62
```

Šie statiskie lauki ir globāli, kopēji visiem objektiem. To maiņa arī notiek globāli:

```js
Person.retirementAge = 62;
console.log(Person.retirementAge); // 62
```

> Piezīme. Pie šādiem statiskiem datiem nevar piekļūt caur `.this`. Jānorāda klases nosaukums un vajadzīga lauka nosaukumu.

```js
print(){ 
    console.log(`Имя: ${this.name}  Возраст: ${this.age}`); 
    console.log(`Пенсионный возраст: ${Person.retirementAge}`);
}
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Статические поля и методы](https://metanit.com/web/javascript/4.17.php)
Iepriekšēja lapa >>> [[Navigācija - Statiskie lauki un metodes]]
Nākama lapa >>> [[Statiskas metodes]]

---