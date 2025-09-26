___

**Datums:** 2025-08-16
**Laiks:** 14:44
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Kļūdu tipu izmantošana

Šeit var apskatīt kā izmantot un apstrādāt kļūdas kodā. Lai piešķirt kļūdas ziņojmu kādam kļūdas tipam, izmanto operatoru `throw new`, un `catch` blokā, lai apstrādāt noteiktu kļūdu, izmanto `instanceof` un norādi kļūdas tipu.

```js
class Person{
  
    constructor(pName, pAge){
         
        const age = parseInt(pAge);
        if(isNaN(age))  throw new TypeError("Возраст должен представлять число");
        if(age < 0 || age > 120) throw new RangeError("Возраст должен быть больше 0 и меньше 120");
        this.name = pName;
        this.age = age;
    }
    print(){ console.log(`Name: ${this.name}  Age: ${this.age}`);}
}
     
try{
    const tom = new Person("Tom", -45);
    const bob = new Person("Bob", "bla bla");
}
catch(error){   
    if (error instanceof TypeError) {
        console.log("Некорректный тип данных.");
    } else if (error instanceof RangeError) {
        console.log("Недопустимое значение");
    }
    console.log(error.message);
}
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Типы ошибок](https://metanit.com/web/javascript/16.3.php)
Iepriekšēja lapa >>> [[Kļūdu tipi]]
Nākama lapa >>> [[Savu kļūdu tipu veidošana]]

---