___

**Datums:** 2025-08-13
**Laiks:** 18:31
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Datu konvertācija

`JavaScript` valodā pastāv 3 konvertācijas veidi:

- automātiska;
- manuāla, izmantojot speciālas metodes;
- operatori `+`, `-`.

##### Automātiska

Tā notiek, kad mēģina saskaitīt skaitlisko un teksta vērtības.

```js
const number1 = "56";
const number2 = 4;
cont result = number1 + number2;
console.log(result); // 564
```

##### Metodes

###### `parseInt()`

```js
const number1 = "56";
const number2 = 4;
const result = parseInt(number1) + number2;
console.log(result); // 60
```

Šādai konvertācijai ir viena īpatnība. Ja teksta rinda saturēs burtus vai speciālus simbolus, metode mēģinās konvertēt skaitļus līdz pirmam šādam simbolam.

```js
const num1 = "123hello";
const num2 = parseInt(num1);
console.log(num2); // 123
```

Ja nu metodei `parseInt()` neizdodas veikt konvertāciju, tā atgriež vērtību `NaN` (Not a Number).

Metode `isNaN()` ļauj pārbaudīt, vai teksta virkne ir skaitlis.

```js
const num1 = "javascript";
const num2 = "22";
let result = isNaN(num1);
console.log(result); // true - num1 не является числом
     
result = isNaN(num2);
console.log(result); //  false - num2 - это число
```

###### `parseFloat()`

Darbojas tāpat kā `parseInt()`.

```js
const number1 = "46.07";
const number2 = "4.98";
let result = parseFloat(number1) + parseFloat(number2);
console.log(result); //51.05
```

###### `toString()`

Konvertācija uz `string`:

```js
let num = 15;  
let text = num.toString();
```

##### Operatori `+` un `-`

```js
const number1 = "56";
const number2 = 4;
const result = +number1 - number2;
console.log(result); // 52
```

Operators `-` atgriež negatīvu vērtību, skaitli ar pretējo zīmi.

```js
const number1 = "56";
const number2 = 4;
const result = -number1 - number2;  // -56 - 4 = -60
console.log(result); // -60
```

Ja konvertācija neizdodas, atgriež `NaN` vērtību.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Преобразование данных](https://metanit.com/web/javascript/2.4.php)
Iepriekšēja lapa >>> [[Operators ??]]
Nākama lapa >>> [[Ievads masīvos]]

---