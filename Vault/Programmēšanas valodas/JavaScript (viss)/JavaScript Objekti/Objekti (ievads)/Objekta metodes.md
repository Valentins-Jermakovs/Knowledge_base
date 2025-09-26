___

**Datums:** 2025-09-09
**Laiks:** 10:09
❚ **Tagi:** #javascript 

---
### Objekta metodes

Metodes nosaka objekta uzvedību, lai noteikt metodes, tiek izmantotas šādas pieejas:

- kad objekts tiek veidots pakāpeniski:

```js
const user = {};
user.name = "Tom";
user.age = 26;
user.display = function(){
     
    console.log(user.name);
    console.log(user.age);
};
 
// вызов метода
user.display();
```

- objekta inicializācijas laikā (mūsdienās visvairāk izmantota pieeja):

```js
const user = {
  
    name: "Tom",
    age: 26,
    display: function(){
      
        console.log(this.name);
        console.log(this.age);
    }
};
```

Šīm veidam eksistē arī īsa pieraksta forma metožu veidošanai:

```js
let user = {
  
    name: "Tom",
    age: 26,
    display(){
      
        console.log(this.name, this.age);
    },
    move(place){
        console.log(this.name, "goes to", place);
    }
};
user.display(); // Tom 26
user.move("the shop");  // Tom goes to the shop
```

Atslēgvārds `this` norāda uz šī objekta laukiem, līdzīgi kā klasēs.

---
### ⇄ Saistības

Avots >>> [JavaScript \| Объекты](https://metanit.com/web/javascript/4.1.php)
Iepriekšēja lapa >>> [[Objekta īpašības]]
Nākama lapa >>> [[Masīvu sintakse]]

---