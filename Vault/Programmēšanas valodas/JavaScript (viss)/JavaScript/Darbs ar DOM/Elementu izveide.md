___

**Datums:** 2025-08-17
**Laiks:** 14:26
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Elementu izveide

Elementu izveidošania tiek izmantotas 2 metodes:

- **createElement(elementName)** - veido `html` elementu, kā parametru saņem tagu, atgriež elementu;
- **createTextNode(text)** - veido un atgriež teksta mezglu, kā parametru saņem tekstu.

##### Metode `createElement`

```js
const header = document.createElement("h1");        // создаем заголовок <h1>
console.log(header);  // <h1></h1>
```

##### Metode `createTextNode`

```js
const headerText = document.createTextNode("Hello World"); // создаем текстовый узел
console.log( headerText);  // "Hello World"
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Создание, добавление, замена и удаление элементов](https://metanit.com/web/javascript/8.5.php)
Iepriekšēja lapa >>> [[Navigācija JavaScript]]
Nākama lapa >>> [[Elementu pievienošana]]

---