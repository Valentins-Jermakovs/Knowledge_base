___

**Datums:** 2025-08-28
**Laiks:** 14:56
❚ **Tagi:** #javascript 

---
### Klases lauki un īpašība


> [!NOTE] Klases lauki
> Lauki ir klases mainīgie.


> [!NOTE] Klases īpašības
> Klases publiskie lauki ir klases īpašības.

Klases lauki tiek izmantoti, lai glabāt kādu informāciju:

```js
class Person{
    name;
    age;
}
const tom = new Person();
tom.name = "Tom";
tom.age = 37;
console.log(tom.name);  // Tom
console.log(tom.age);   // 37
```

Pēc objekta izveides, caur punktu `.` mēs varam vērsties pie objekta laukiem:

```js
tom.name = "Tom";       // установим значение поля
console.log(tom.name);  // получим значение свойства
```

Nepieciešamības pēc mēs varam iestatīt noklusējuma vērtības klases laukiem:

```js
class Person{
    name = "Unknown";
    age= 18;
}
const tom = new Person();
console.log(tom.name);  // Unknown
tom.name = "Tom";
console.log(tom.name);  // Tom
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Классы](https://metanit.com/web/javascript/4.12.php)
Iepriekšēja lapa >>> [[Objektu izveide]]
Nākama lapa >>> [[Klases uzvedība un tās metodes]]

---