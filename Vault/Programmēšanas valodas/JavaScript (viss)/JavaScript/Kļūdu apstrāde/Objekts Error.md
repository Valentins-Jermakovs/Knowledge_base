___

**Datums:** 2025-08-16
**Laiks:** 14:35
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts

#### Objekts `Error`

`Error` obejtam ir šādas īpašības, ko var izmantot kļūdu apstrādē:

- `message` - ziņojums par kļūdu;
- `name` - kļūdas tips;
- `fileName` - faila nosaukums, kur notika `JavaScript` kļūda;
- `lineNumber` - līnija failā, kur notika kļūda;
- `columnNumber` - kolonna koda rindā, kur notika kļūda;
- `stack` - kļūdas steks.

Koda piemērs:

```js
try{
    callSomeFunc();
}
catch(error){
    console.log("Тип ошибки:", error.name);
    console.log("Ошибка:", error.message);
}
```

```
Тип ошибки: ReferenceError
Ошибка: callSomeFunc is not defined
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Типы ошибок](https://metanit.com/web/javascript/16.3.php)
Iepriekšēja lapa >>> [[Kļūdu ģenerēšana un operators throw]]
Nākama lapa >>> [[Kļūdu tipi]]

---