___

**Datums:** 2025-08-16
**Laiks:** 13:58
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Virknes paplašināšana

Šīs metodes ļāuj paplašināt teksta virnki ievietojot frāzes, vārdus vai siimbolus sākumā/beigās:

- `padStart()` - ievieto simbolus sākumā;
- `padEnd()` - ievieto simbolus beigās.

Metodes pieņem šādus parametrus:

- teksta virkne, kura tiks paplašināta;
- skaitlis - daudzums, simbolu summa  (šeit jāpiemin, kā metodei vajag nodot teksta virknes simbolu skaitu + simbolu skaitu, kurus gribi pievienot);
- simbols/teksts, kas tiks pievienots.

Piemērs, ja norādi tikai skaitli, pēc noklusējuma pievieno `space`.

```js
let hello = "hello".padStart(8);  // "   hello"
console.log(hello);
hello = "hello".padEnd(8);      // "hello   "
console.log(hello);
```

Šeit piemēri, kad jau norādi otro parametru:

```js
let hello = "hello".padStart(17, "JavaScript, ");  // "JavaScript, hello"
hello = "hello".padEnd(12, " Eugene");      // "hello Eugene"
```

```js
let hello = "123".padStart(6, "0");  // "000123"
hello = "123".padEnd(6, "0");       // "123000"
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Строки](https://metanit.com/web/javascript/6.1.php)
Iepriekšēja lapa >>> [[Pārbaude uz sākumu, beigām]]
Nākama lapa >>> [[Navigācija JavaScript]]

---