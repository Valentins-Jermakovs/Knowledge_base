___

**Datums:** 2025-08-16
**Laiks:** 13:37
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### `space` dzēšana

Kopumā, lai izdzēst `space` teksta virknei no abām pusēm, tiek izmantota metode **trim()**. Taču šai metodei ir arī apakšmetodes, kas darbojas uz kādu konkrētu virzienu:

- `trimStart()` - izdzēš `space` no virknes sākumā (atkarībā no tā kā tiek rakstīts, no labi pa kreisi vai otrādi, darbība atkarīga no rakstīšanas sistēmas);
- `trimEnd()` - izdzēš `space` no virknes beigām (atkarībā no tā kā tiek rakstīts, no labi pa kreisi vai otrādi, darbība atkarīga no rakstīšanas sistēmas);
- `trimLeft()` - izdzēš `space` no kreisās puses;
- `trimRight()` - izdzēš `space` no labās puses.

```js
let hello = "   Привет Том  ";
const beforeLength = hello.length;
hello = hello.trim();
const afterLength = hello.length;
console.log("Длина строки до: ", beforeLength);     // 15
console.log("Длина строки после: ", afterLength);   // 10
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Строки](https://metanit.com/web/javascript/6.1.php)
Iepriekšēja lapa >>> [[Simbolu iegūšana pēc indeksa]]
Nākama lapa >>> [[Virkņu apvienošana]]

---