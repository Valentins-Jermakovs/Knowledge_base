___

**Datums:** 2025-08-16
**Laiks:** 17:58
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Datumu noteikšana

Pastāv vairaki veidi, kā izveidot objektu **Date**.

##### Konstruktors bez parametriem

Objekts, kas bija izveidots bez parametriem, glabās informāciju par šodienas datumu.

```js
const currentDate = new Date();
console.log(currentDate);   // Thu Oct 26 2023 13:17:53 GMT+0100
```

##### Konstruktors ar milisekundēm

Datuma konstruktoram tiek nodots milisekundes skaits, kas pagājis kopš Unix laikmeta, tas ir, kopš 1970. gada 1. janvāra plkst. 00:00:00 GMT:

```js
const myDate = new Date(1359270000000);
console.log(myDate); // Sun Jan 27 2013 11:00:00 GMT+0400 (Москва, стандартное время)
```

##### Konstruktors ar dienu, mēnesi, gadu

Ja lietojam pilnu mēneša nosaukumu, tad to raksta angļu valodā, ja saīsināto versiju, tad tiek izmantots formāts "mēnesis/diena/gads" vai "mēnesis diena gads".

```js
const date1 = new Date("27 March 2008");
console.log(date1); // Thu Mar 27 2008 00:00:00 GMT+0300 (Москва, стандартное время)
// или так
const date2 = new Date("3/27/2008");
console.log(date2); // Thu Mar 27 2008 00:00:00 GMT+0300 (Москва, стандартное время)
// или так
const date3 = new Date("3 27 2008");
console.log(date3); // Thu Mar 27 2008 00:00:00 GMT+0300 (Москва, стандартное время)
```

##### Konstruktors ar visiem parametriem

Šajā gadījumā secībā tiek izmantoti šādi parametri: **new Date**(gads, mēnesis, diena, stunda, minūtes, sekundes, milisekundes). Jāatzīmē, ka mēneši tiek skaitīti no nulles, t. i., janvāris ir `0`, bet decembris ir `11`.

```js
const myDate = new Date(2012,11,25,18,30,20,10); 
console.log(myDate); // Tue Dec 25 2012 18:30:20 GMT+0400 (Москва, стандартное время)
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объект Date. Работа с датами](https://metanit.com/web/javascript/5.1.php)
Iepriekšēja lapa >>> [[Datumu noteikšana (objekta izveidošana)]]
Nākama lapa >>> [[Datuma un laika iegūšana]]

---