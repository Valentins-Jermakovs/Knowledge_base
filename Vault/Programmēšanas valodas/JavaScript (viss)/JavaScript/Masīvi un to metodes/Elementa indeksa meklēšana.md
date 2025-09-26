___

**Datums:** 2025-08-15
**Laiks:** 11:39
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Elementa indeksa meklēšana

Pastāv divas metodes:

- `indexOf()` - atgriež pirmās sakritības indeksu;
- `lastIndexOf()` - atgriež pēdējo sakritību.

```js
const people = ["Tom", "Sam", "Bob", "Tom", "Alice", "Sam"];
 
const firstIndex = people.indexOf("Tom");
const lastIndex = people.lastIndexOf("Tom");
const otherIndex = people.indexOf("Mike");
console.log(firstIndex); // 0
console.log(lastIndex);  // 3
console.log(otherIndex); // -1
```

Ja meklējamais elements neeksistē, abas metodes atgriež `-1`.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Операции с массивами](https://metanit.com/web/javascript/5.7.php)
Iepriekšēja lapa >>> [[Kārtošana pretējā virzienā]]
Nākama lapa >>> [[Pārbaude uz elementa esamību]]

---