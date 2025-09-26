___

**Datums:** 2025-08-16
**Laiks:** 18:13
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Datuma un laika iestatīšana

Mēs varam iestatīt laika datus objektam **Date** izmantojot ne tikai parametrus, bet arī metodes:

|Metode|Apraksts|
|---|---|
|**setDate()**|Uzstāda mēneša dienu|
|**setMonth()**|Uzstāda mēnesi (skaitīšana sākas no 0, tātad 0 – janvāris)|
|**setFullYear()**|Uzstāda gadu|
|**setHours()**|Uzstāda stundu|
|**setMinutes()**|Uzstāda minūtes|
|**setSeconds()**|Uzstāda sekundes|
|**setMilliseconds()**|Uzstāda milisekundes|

Piemērs ar datuma uzstadīšanu:

```js
const myDate = new Date();
myDate.setDate(14);
myDate.setMonth(10);    // ноябрь
myDate.setFullYear(2023); 
console.log(myDate); // Tue Nov 14 2023 13:41:20 GMT+0300 (Москва, стандартное время)
```

Iestatot vērtības, mēs varam nodot vērtību, kas ir lielāka par maksimāli pieļaujamo vērtību. Piemēram, iestatot stundu uz 54:

```js
myDate.setHours(54);
```

Šajā gadījumā stundas vērtība būs 54 - 24 * 2 = 6, un atlikušās stundas būs divas dienas (24 * 2), kas datumam pievienos divas dienas. Tas pats attiecas uz dienām, minūtēm, sekundēm, milisekundēm un mēnešiem.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объект Date. Работа с датами](https://metanit.com/web/javascript/5.1.php)
Iepriekšēja lapa >>> [[Datuma un laika iegūšana]]
Nākama lapa >>> [[Objekts Math]]

---