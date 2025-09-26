___

**Datums:** 2025-08-14
**Laiks:** 15:59
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Bultu funkcijas

##### Ievads

Tā ir īsa funkcijas pieraksta forma. Sintakse izskatās šādi:

```js
(parametri) => funkcijas_instrukcijas
```

Standarta funkcijas pieraksts:

```js
function hello(){
    console.log("Hello");
}
hello();    // вызываем функцию
```

Bultu funkcijas variants tai pašai funkcijai:

```js
const hello = ()=> console.log("Hello");
hello();
```

Šeit `()=>` ir tukšs, jo nekādus parametrus mēs nenododam.

##### Parametru nodošana

Piemērs, kur nododam vienu parametru:

```js
const print = (mes)=> console.log(mes);
 
print("Hello Metanit.com");
print("Welcome to JavaScript");
```

Piemērs ar diviem parametriem:

```js
const sum = (x, y)=> console.log("Sum =", x + y);
 
sum(1, 2);      // Sum = 3
sum(4, 3);      // Sum = 7
sum(103, 2);    // Sum = 105
```
##### Rezultāta atgriešana

Lai atgriezt rezultātu, šajā pierakstā netiek izmantots `return`.

```js
const sum = (x, y)=> x + y;
 
console.log(sum(1, 2));     // 3
console.log(sum(4, 3));     // 7
console.log(sum(102, 5));   // 107
```

```js
const hello = name => `Hello, ${name}`;
 
console.log(hello("Tom"));              // Hello, Tom
console.log(hello("Bob"));              // Hello, Bob
console.log(hello("Frodo Baggins"));    // Hello, Frodo Baggins
```

*Piezīme. Ja funkcijai tiek nodots tikai 1 parametrs, to nav obligāti jāieraksta `()` iekavās.*
##### Objekta atgriešana

Lai atgriest objektu, tas tiek ierakstīts `({})` apaļās un pēc tam figūriekavās.

```js
const user = (userName, userAge) => ({name: userName, age: userAge});
 
let tom = user("Tom", 34);
let bob = user("Bob", 25);
 
console.log(tom.name, tom.age);     // "Tom", 34
console.log(bob.name, bob.age);     // "Bob", 25
```

##### Funkcija ar vairākām instrukcijām

Augstāk minētos piemēros funkcijām bija tikai viena instrukcija. Šādi izskatāš ar vairāk instrukcijām.

```js
const square = n => {
    const result = n * n;
    console.log(result);
}
  
square(5);     // 25
square(6);     // 36
```

Nu un šeit vajag izmantot `return`, lai atgriezt funkcijas rezultātu.

```js
const square = n => {
    const result = n * n;
    return result;
}
  
console.log(square(5));     // 25
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Стрелочные функции](https://metanit.com/web/javascript/3.8.php)
Iepriekšēja lapa >>> [[Funkcijas rezultāts]]
Nākama lapa >>> [[Funkcijas, kas pašas sevi izsauc]]

---