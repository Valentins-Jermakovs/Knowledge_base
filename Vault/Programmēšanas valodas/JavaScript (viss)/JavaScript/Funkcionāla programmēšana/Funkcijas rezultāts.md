___

**Datums:** 2025-08-14
**Laiks:** 15:55
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Funkcijas rezultāts

Izmantojot metodi `return`, funkcija var atgriest vērtību, rezultātu.

```js
function sum (a, b) {
  return a + b;
}
let num1 = sum(2, 4);
console.log(num1);  // 6
 
const num2 = sum(6, 34);
console.log(num2);  // 40
```

Funkcija var atgriezt tikai vienu vērtību, tāpēc, ja to mums ir vairāk, tās ieraksta masīvā.

```js
function rectangle(width, height){
 
    const perimeter = width *2 + height * 2;
    const area = width * height;
    return [perimeter, area];
}
 
const rectangleData = rectangle(20, 30);
console.log(rectangleData[0]);  // 100 - периметр прямоугольника
console.log(rectangleData[1]);  // 600 - площадь прямоугольника
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Результат функции](https://metanit.com/web/javascript/3.11.php)
Iepriekšēja lapa >>> [[Funkcijas kā parametri]]
Nākama lapa >>> [[Bultu funkcijas (стрелочные функции)]]

---