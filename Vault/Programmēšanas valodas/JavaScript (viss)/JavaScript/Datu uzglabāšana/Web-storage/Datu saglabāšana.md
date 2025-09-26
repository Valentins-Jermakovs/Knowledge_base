___

**Datums:** 2025-08-30
**Laiks:** 14:03
❚ **Tagi:** #javascript 

---
### Datu saglabāšana

Datu saglabāšanai tiek izmantota metode `setItem()`, kas pieņem atslēgu un vērtību. Jāpiemin, kā visi dati tiek pārveidoti uz `string` datu tipu.

```js
localStorage.setItem("email", "tom32@gmail.com");
sessionStorage.setItem("username", "Tom Smith");
```

Ja mums nepieciešams saglabāt kādus sarežģītākus datus, tad tos būtu ieteicams serializēt uz objektu formātā JSON:

```js
const user ={
    name: "Tom",
    age: 23,
    isMarried: false
};
 
localStorage.setItem("user", JSON.stringify(user));
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Web Storage](https://metanit.com/web/javascript/12.2.php)
Iepriekšēja lapa >>> [[Programmēšanas valodas/JavaScript (viss)/JavaScript/Datu uzglabāšana/Web-storage/Ievads|Ievads]]
Nākama lapa >>> [[Datu ieguve]]

---