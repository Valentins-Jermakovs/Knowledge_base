___

**Datums:** 2025-08-16
**Laiks:** 18:06
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Datuma un laika iegūšana

|Metode|Apraksts|
|---|---|
|**getDate()**|Atgriež mēneša dienu|
|**getDay()**|Atgriež nedēļas dienu (skaitīšana sākas no 0 – svētdiena, un pēdējā diena ir 6 – sestdiena)|
|**getMonth()**|Atgriež mēneša numuru (skaitīšana sākas no 0, tātad 0 – janvāris)|
|**getFullYear()**|Atgriež gadu|
|**toDateString()**|Atgriež pilnu datumu kā virkni|
|**getHours()**|Atgriež stundu (no 0 līdz 23)|
|**getMinutes()**|Atgriež minūtes (no 0 līdz 59)|
|**getSeconds()**|Atgriež sekundes (no 0 līdz 59)|
|**getMilliseconds()**|Atgriež milisekundes (no 0 līdz 999)|
|**toTimeString()**|Atgriež pilnu laiku kā virkni|

Piemērs ar šodienas datuma saņemšanu:

```js
const today = new Date(); 
console.log(today.getDate());       // 26
console.log(today.getDay());        // 4
console.log(today.getMonth());      // 9
console.log(today.getFullYear());   // 2023
```

Pēc datu iegūšanas konvertējam tos uz ērtāk lasāmu formātu:

```js
const days = ["Воскресенье", "Понедельник", "Вторник", "Среда", "Четверг", "Пятница", "Суббота"];
const months = ["Январь", "Февраль", "Март", "Апрель", "Май", "Июнь", 
            "Июль", "Август", "Сентябрь", "Октябрь", "Ноябрь", "Декабрь"];
 
const today = new Date(); 
console.log(`Сегодня: ${today.getDate()} ${months[today.getMonth()]} ${today.getFullYear()}, ${days[today.getDay()]}`);
// Сегодня: 26 Октябрь 2023, Четверг
```

Piemērs ar tagadēja laika datu ieguvi:

```js
var welcome;
const myDate = new Date();
const hour = myDate.getHours();
const minute = myDate.getMinutes();
const second = myDate.getSeconds();
 
console.log(`Текущее время: ${hour}:${minute}:${second}`); // Текущее время: 13:38:26
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объект Date. Работа с датами](https://metanit.com/web/javascript/5.1.php)
Iepriekšēja lapa >>> [[Datumu noteikšana (objekta izveidošana)]]
Nākama lapa >>> [[Datuma un laika iestatīšana]]

---