___

**Datums:** 2025-08-30
**Laiks:** 12:29
❚ **Tagi:** #javascript 

---
### Moduļa pieslēgšana

Tagad tiks parādīts, kā pieslēgt iepriekš veidoto [moduli](obsidian://open?vault=Vault&file=Kursi%20(struktur%C4%93ts)%2FJavaScript%2FModu%C4%BCi%2FIevads%20modu%C4%BCos%2FModu%C4%BCa%20noteik%C5%A1ana%20(eksports)). Priekš tā izveidosim failu `main.js` un ievietosim šo kodu:

```js
import {sayHello} from "./message.js";
sayHello();
```

Pieslēgšanai tiek izmantots atslēgas vārds `import`, pēc kura tiek pieslēdzamo moduļu nosaukumi. Visi moduļi, kas tiek pieslēgti, tiek ievietoti fugūriekavās `{}`.

Pēc operātora **from** tiek norādīts modulis, no kura tiek veikts imports `./message.js`.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Введение в модули](https://metanit.com/web/javascript/19.1.php)
Iepriekšēja lapa >>> [[Moduļa noteikšana (eksports)]]
Nākama lapa >>> [[Moduļa ielāde]]

---