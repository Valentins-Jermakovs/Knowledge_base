___

**Datums:** 2025-08-16
**Laiks:** 18:20
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Matemātiskas metodes

Objekts **Math** piedāvā vairākas matemātiskas funkcijas, ko var izmantot skaitļošanā:

| Metode    | Ko dara?                                                   |
| --------- | ---------------------------------------------------------- |
| `abs()`   | Atgriež skaitļa absolūto vērtību (bez zīmes)               |
| `min()`   | Atgriež mazāko skaitli no argumentiem                      |
| `max()`   | Atgriež lielāko skaitli no argumentiem                     |
| `ceil()`  | Noapaļo skaitli uz augšu līdz tuvākajam veselajam skaitlim |
| `floor()` | Noapaļo skaitli uz leju līdz tuvākajam veselajam skaitlim  |
| `round()` | Noapaļo skaitli līdz tuvākajam veselajam skaitlim          |
| `pow()`   | Aprēķina skaitļa pakāpi (`pow(x, y)` → _x^y_)              |
| `sqrt()`  | Aprēķina kvadrātsakni                                      |
| `log()`   | Atgriež naturālo logaritmu (ln)                            |
| `sin()`   | Aprēķina sinus vērtību                                     |
| `cos()`   | Aprēķina kosinus vērtību                                   |
| `tan()`   | Aprēķina tangens vērtību                                   |
| `asin()`  | Atgriež arksinusu (rezultāts radiānos)                     |
| `acos()`  | Atgriež arkkosinusu (rezultāts radiānos)                   |
| `atan()`  | Atgriež arktangensu (rezultāts radiānos)                   |

Zemāk tiek apskatīti piemēri ar šīm matemātiskām funkcijām.

##### abs()

Atgriež absolūto vērtību:

```js
const x = -25;
console.log(Math.abs(x)); // 25
const y = 34;
console.log(Math.abs(y)); // 34
```

##### min() un max()

```js
const max = Math.max(19, 45); // 45
const min = Math.min(33, 24); // 24
// var pieņemt vairāk par 2 skaitļiem
const max = Math.max(1, 2, 3, -9, 46, -23); // 46
```

##### ceil()

Noapaļo līdz tuvākam lielākam skaitlim:

```js
const x = Math.ceil(9.2); // 10
const y = Math.ceil(-5.9); // -5
```

##### floor()

Noapaļo līdz mazākām veselam skaitlim:

```js
const x = Math.floor(9.2); // 9
const y = Math.floor(-5.9); // -6
```

##### round()

Ja mazāk par `0.5` noapaļo uz mazāko, ja vairāk, uz lielāko:

```js
const x = Math.round(5.5); // 6
const y = Math.round(5.4); // 5
const z = Math.round(-5.4); // -5
const n = Math.round(-5.5); // -5
const m = Math.round(-5.6); // -6
console.log(x);
console.log(y);
console.log(z);
console.log(n);
```

##### random()

Atgriež decimālskaitli no `0` līdz `1`.

```js
const x = Math.random();
```

##### pow()

Atgriež kāpinājumu. Šeit `2` tiek celts `3` pakāpē:

```js
const x = Math.pow(2, 3); // 8 jeb 2^3
```

##### sqrt()

Atgriež kvadrātsakni:

```js
const x = Math.sqrt(121); // 11
const y = Math.sqrt(9); // 3
const z = Math.sqrt(20); // 4.47213595499958
```

##### log()

Atgriež logarifmu:

```js
const x = Math.log(1); // 0
const z = Math.log(10); // 2.302585092994046
```

##### Konstantes

| Konstante         | Ko dara?                       | Vērtība              |
| ----------------- | ------------------------------ | -------------------- |
| **Math.PI**       | Skaitlis π (pi)                | `3.141592653589793`  |
| **Math.SQRT2**    | Kvadrātsakne no 2              | `1.4142135623730951` |
| **Math.SQRT1\_2** | Puse no kvadrātsaknes no 2     | `0.7071067811865476` |
| **Math.E**        | Skaitlis *e* (Eilera skaitlis) | `2.718281828459045`  |
| **Math.LN2**      | Naturālais logaritms no 2      | `0.6931471805599453` |
| **Math.LN10**     | Naturālais logaritms no 10     | `2.302585092994046`  |
| **Math.LOG2E**    | Divnieka logaritms no *e*      | `1.4426950408889634` |
| **Math.LOG10E**   | Desmitnieka logaritms no *e*   | `0.4342944819032518` |
```js
const x = Math.log(Math.E); // 1
const z = Math.tan(Math.PI/4); // 0.9999999999999999
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объект Math. Математические операции](https://metanit.com/web/javascript/5.2.php)
Iepriekšēja lapa >>> [[Datuma un laika iestatīšana]]
Nākama lapa >>> [[Navigācija JavaScript]]

---