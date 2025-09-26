___

**Datums:** 2025-08-16
**Laiks:** 13:52
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Pārbaude uz sākumu, beigām

Lai pārbaudīt, vai teksta virkne sākas, beidzās ar konkrētu vārdu, tiek izmantotas 2 metodes:

- `startsWith()` - meklē sākumā;
- `endsWith()` - meklē beigās.

Kā pirmo parametru metodes pieņem meklējamo vārdu (obligāts parametrs).

```js
const hello = "let me speak from my heart";
console.log(hello.startsWith("let"));       // true
console.log(hello.startsWith("Let"));       // false
console.log(hello.startsWith("lets"));      // false
 
console.log(hello.endsWith("heart"));       // true
console.log(hello.startsWith("bart"));      // false
```

Kā otro parametru var nodot indeksu, no kura sākas meklēšana (neobligāts parametrs).

```js
const hello = "let me speak from my heart";
console.log(hello.startsWith("me", 4));     // true, "me" - 4 индекс с начала строки
 
console.log(hello.startsWith("my", hello.length-8));    // true, "my" - 8 индекс с конца
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Строки](https://metanit.com/web/javascript/6.1.php)
Iepriekšēja lapa >>> [[Virknes dalīšana]]
Nākama lapa >>> [[Virknes paplašināšana]]

---