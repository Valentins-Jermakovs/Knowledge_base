___

**Datums:** 2025-08-16
**Laiks:** 13:45
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Apakšrindas maiņa

Lai mainīt teksta virknes saturu, tiek izmantotas divas metodes:

- `replace()` - veic maiņu pirmai sakritībai;
- `replaceAll()` - veic maiņu visām sakritībām.

Abas metodes pieņem 2 parametrus:

- `pirmais_parametrs` - norāda, kādu apakšrindu vajag aizvietot;
- `otrais_parametrs` - norāda, uz ko vajag aizvietot.

##### Metode `replace()`

```js
let menu = "Завтрак: каша, чай. Обед: суп, чай. Ужин: салат, чай.";
menu = menu.replace("чай", "кофе");
console.log(menu);  // Завтрак: каша, кофе. Обед: суп, чай. Ужин: салат, чай.
```

Aizvieto tikai pirmo sakritību.

##### Metode `replaceAll()`

```js
let menu = "Завтрак: каша, чай. Обед: суп, чай. Ужин: салат, чай.";
menu = menu.replaceAll("чай", "кофе");
console.log(menu);  // Завтрак: каша, кофе. Обед: суп, кофе. Ужин: салат, кофе.
```

Aizvieto visas sakritības.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Строки](https://metanit.com/web/javascript/6.1.php)
Iepriekšēja lapa >>> [[Virkņu apvienošana]]
Nākama lapa >>> [[Virknes dalīšana]]

---