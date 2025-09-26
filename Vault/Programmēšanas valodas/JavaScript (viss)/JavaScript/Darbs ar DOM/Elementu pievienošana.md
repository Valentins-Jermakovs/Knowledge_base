___

**Datums:** 2025-08-17
**Laiks:** 14:30
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Elementu pievienošana

Elementu pievienošainai pie esošiem objektiem tiek izmantotas šādas metodes:

- `appendChild(newNode)` - pievieno jauno mezglu/elementu beigās;
- `insertBefore(newNode, referenceNode)` - pievieno jauno mezglu/elementu `newNode` pirms `referenceNode` elementa/mezgla.

##### Metode `appendChild`

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
    <script>
    constheader = document.createElement("h1");     // создаем заголовок <h1>
    const headerText = document.createTextNode("Hello World");  // создаем текстовый узел
    header.appendChild(headerText); // добавляем в элемент h1 текстовый узел
    document.body.appendChild(header);  // // добавляем элемент h1 на страницу в элемент body
    </script>
</body>
</html>
```

*Piezīme. Teksta saturu var pa taisno uzrakstīt elementam pēc tā izveidošanas, izmantojot metodes `innerText` vai `textContent`.*

```js
const header = document.createElement("h1");        // создаем заголовок <h1>
header.textContent = "Hello World"; // определяем текст элемента
```

##### Metode `insertBefore`

Šī metode ļauj mums ievietot jaunizveidoto elementu konkrētā pozīcijā. Piemērā jaunais elements tiek izvietots pirms pirmā paragrāfa:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
    <p>Text 1</p>
    <p>Text 2</p>
    <script>
    const header = document.createElement("h1");        // создаем заголовок <h1>
    header.textContent = "Page Header"; // определяем текст элемента
    // получаем первый параграф
    const firstP = document.body.firstElementChild;
    // добавляем элемент h1 перед параграфом firstP
    document.body.insertBefore(header, firstP); 
    </script>
</body>
</html>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Создание, добавление, замена и удаление элементов](https://metanit.com/web/javascript/8.5.php)
Iepriekšēja lapa >>> [[Elementu izveide]]
Nākama lapa >>> [[Elementu kopēšana]]

---