___

**Datums:** 2025-08-16
**Laiks:** 18:37
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### JSON dati

Šādi izskatās `JSON` dokuments. Tas var saturēt kā masīvus, tā arī citus `JSON` dokumentus:

```json
{
    "name": "Tom",
    "married": true,
    "age": 30
}
```

```json
{
    "name": "Tom",
    "married": true,
    "age": 30,
    "company": {
        "name": "Microsoft",
        "address": "USA, Redmond"
    }
}
```

```json
[{
    "name": "Tom",
    "married": true,
    "age": 30
},{
    "name": "Alice",
    "married": false,
    "age": 23
}]
```

##### Serializācija

Serializācija - kad `JavaScript` objektu konvertē uz `JSON` dokumentu:

```js
// объект javascript
const user = {
    name: "Tom",
    married: false,
    age: 39
};
// объект json
const serializedUser = JSON.stringify(user);
console.log(serializedUser); // {"name":"Tom","married":false,"age":39}
```

##### Deserializācija

Šeit ir pretējs process, no `JSON` dokumenta uz `JavaScript` objektu:

```js
const user = {
    name: "Tom",
    married: false,
    age: 39
};
// сериализация - konvertē uz JSON
const serializedUser = JSON.stringify(user);
// десериализация - konvertē uz JavaScript objektu
const tomUser = JSON.parse(serializedUser);
console.log(tomUser.name); // Tom - piekļūst objekta datiem
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Работа с JSON](https://metanit.com/web/javascript/11.1.php)
Iepriekšēja lapa >>> [[Navigācija JavaScript]]

---