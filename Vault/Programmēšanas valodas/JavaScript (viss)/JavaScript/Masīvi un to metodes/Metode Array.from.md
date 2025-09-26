___

**Datums:** 2025-08-14
**Laiks:** 17:04
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### `Array.from`

šī metode ļauj izveidot masīvu no masīva, masīva līdzīgiem elementiem. Piemēram sadalīt teksta virkni uz masīvu:

```js
const array = Array.from("Hello");
console.log(array); // ["H", "e", "l", "l", "o"]
```

Kā otru parametru var nodot funkciju, kas modificēs nodotos elementus:

```js
const numbers = [1, 2, 3, 4];
const array = Array.from(numbers, n => n * n);
console.log(array); // [1, 4, 9, 16]
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Создание массива и объект Array](https://metanit.com/web/javascript/5.3.php)
Iepriekšēja lapa >>> [[Masīva izveide]]
Nākama lapa >>> [[length metode]]

---