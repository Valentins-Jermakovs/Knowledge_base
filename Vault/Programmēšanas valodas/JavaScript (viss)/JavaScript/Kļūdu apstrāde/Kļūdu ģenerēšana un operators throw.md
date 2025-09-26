___

**Datums:** 2025-08-16
**Laiks:** 14:28
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Kļūdu ģenerēšana

Operators `throw` ļauj mums veidot savus kļūdu ziņojumus:

```js
class Person{
  
    constructor(name, age){
        if(age < 0) throw "Возраст должен быть положительным";
        this.name = name;
        this.age = age;
    }
    print(){ console.log(`Name: ${this.name}  Age: ${this.age}`);}
}
     
try{
    const tom = new Person("Tom", -123);    // Uncaught Возраст должен быть положительным
    tom.print();
}
catch(error){
    console.log("Произошла ошибка");
    console.log(error);     // Возраст должен быть положительным
}
```

Piemērs ar datu bāzes imitāciju:

```js
// класс условной базы данных
class Database{
    constructor(){
        this.data = ["Tom", "Sam", "Bob"];
    }
    // получение данных
    getItem(index){ 
        this.open();
        if(index > 0 && index < this.data.length)
            return this.data[index];
        else
            throw "Некорректный индекс";
        this.close();   // при генерации исключения эта строка не будет выполняться
    }
    // открытие бд
    open(){ console.log("Подключение к базе данных установлено"); }
    // закрытие бд
    close(){ console.log("Подключение к базе данных закрыто"); }
}
 
const db = new Database();
try {
    db.getItem(5);   // возвращаем полученный элемент
} catch(err) {
    console.error(err); // если произошла ошибка обрабатываем ее 
}
```

```
Подключение к базе данных установлено
Некорректный индекс
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Генерация ошибок и оператор throw](https://metanit.com/web/javascript/16.2.php)
Iepriekšēja lapa >>> [[try...catch...finally konstrukcija]]
Nākama lapa >>> [[Objekts Error]]

---