___

**Datums:** 2025-09-09
**Laiks:** 10:29
❚ **Tagi:** #javascript 

---
### Dinamiska īpašību un metožu nosaukumu noteikšana

Masīvu sintakses pielietojums objekta izveidē, ļauj mums dinamiski noteikt tā īpašību un metožu nosaukumus:

```js
const prop1  = "name";
const prop2  = "age";
const tom = { 
    [prop1]: "Tom",
    [prop2]: 37
};
console.log(tom);           // {name: "Tom", age: 37}
console.log(tom.name);      // Tom
console.log(tom["age"]);    // 37
```

Ko savukārt var izmantot funkcijās, kas atgriež objektu ar mūsu iestatītiem parametriem:

```js
function createObject(propName, propValue){
	// šeit tiek atgriezts objekts
    return {
            [propName]: propValue,
            print(){ 
                console.log(`${propName}: ${propValue}`);
            }
    };
}
const person = createObject("name", "Tom");
person.print();     // name: Tom
 
const book = createObject("title", "JavaScript Reference");
book.print();   // title: JavaScript Reference
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объекты](https://metanit.com/web/javascript/4.1.php)
Iepriekšēja lapa >>> [[Teksta virnknes kā īpašības un metodes]]
Nākama lapa >>> [[Īpašību dzēšana]]

---