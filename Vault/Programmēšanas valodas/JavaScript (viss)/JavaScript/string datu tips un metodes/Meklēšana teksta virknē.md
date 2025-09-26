___

**Datums:** 2025-08-15
**Laiks:** 19:13
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Metodes `indexOf/lastIndexOf`

Metodes:

- `indexOf(str, index)` - atgriež pirmo sakritību;
- `lastIndexOf(str, index)` - atgriež pēdējo sakritību.

Abas pieņem 2 parametrus:

- `str` - apakšrinda, ko vajag meklēt;
- `index` - indekss, no kura sākas meklēšana (neobligāts parametrs).

```js
const hello = "привет мир. пока мир";
const key = "мир";
const firstPos = hello.indexOf(key);
const lastPos = hello.lastIndexOf(key);
console.log("Первое вхождение: ", firstPos);    // 7
console.log("Последнее вхождение: ", lastPos);  // 17
```

Piemērs ar indeksu:

```js
const hello = "привет мир. пока мир";
const key = "мир";
const firstPos = hello.indexOf(key, 10);    // поиск с 10-го индекса
console.log("Первое вхождение: ", firstPos);    // 17
```

*Piezīme. Meklēšana ir jūtīga pret simbolu reģistru. Ja metode neko neatrod, tā atgriež `-1`.*

```js
const hello = "привет мир. пока мир";
const key = "Мир";
const firstPos = hello.indexOf(key);
console.log(firstPos);  // -1
```

#### Metode `includes`

Šī metode atgriež `True` vai `False`, atkarība no tā, vai tā atrod apakšrindu teksta virknē.

```js
const hello = "привет мир. пока мир";
 
console.log(hello.includes("мир")); // true
console.log(hello.includes("миг")); // false
```

Tāpāt kā ar iepriekšējām metodēm, var nodot indeksu, no kura sāksies meklēšana:

```js
const hello = "привет мир. пока мир";
 
console.log(hello.includes("мир", 5));  // true
console.log(hello.includes("привет", 6));   // false
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Строки](https://metanit.com/web/javascript/6.1.php)
Iepriekšēja lapa >>> [[Virknes atkārtošana]]
Nākama lapa >>> [[Apakšrindas izvēle]]

---