___

**Datums:** 2025-08-15
**Laiks:** 12:26
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Metode `reduce()`

Šī metode tiek izmantota, lai apvienot visu masīva elementa vērtības zem vienas vērtības.
Metode var pieņemt līdz 4 parametriem:

- `prev` - iepriekšējais elements (sākuma elements);
- `current` - tagadējais elements (otrais elements);
- `curIndex` - tagadēja elementa indekss;
- `array` - masīvs, priekš kura tiek izsaukta funkcija.

Piemērs, metodes izmantošana visu elementu summas meklēšanai:

```js
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((prev,current) => prev +=current);
console.log(sum);   // 15
```

Papildus var ielikt otro parametru, sākuma vērtību, no kuras sāksies skaitļošana:

```js
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((prev,current) => prev +current, 10);
console.log(sum);   // 25
```

Metode `reduce()` apskata elementus no sākuma līdz beigām `->`, kad metode `reduceRight()` otrādi, no beigām uz sākumu `<-`:

```js
const numbers = [1, 2, 3, 4, 5];
const reduced1 = numbers.reduce((prev,current) => prev +=current.toString());
console.log(reduced1);   // 12345
const reduced2 = numbers.reduceRight((prev,current) => prev +=current.toString());
console.log(reduced2);   // 54321
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Операции с массивами](https://metanit.com/web/javascript/5.7.php)
Iepriekšēja lapa >>> [[Elementu kārtības maiņa ar vecā masīva saglabāšanu]]
Nākama lapa >>> [[Metožu kombinēšanas piemērs]]

---