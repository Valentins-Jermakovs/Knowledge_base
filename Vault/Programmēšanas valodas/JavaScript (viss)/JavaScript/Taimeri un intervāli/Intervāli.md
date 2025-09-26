___

**Datums:** 2025-08-25
**Laiks:** 10:38
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Par intervāliem

Intervāli tiek izmantoti, lai izpildīt funkcijas pēc/ar noteikta/u laika/u.

```JavaScript
setInterval(my_func, 1000) //izsauc my_func pēc 1000 milisekundēm

//otrs veids
var counter = 0;
setInterval(function() {
	console.log("Pagāja " + counter + "sekundes.");
	counter++;
}, 1000);

//lai apstādināt pēc kāda laika intervālu
var counter = 0;

var id = setInterval(my_func, 1000);

function my_func() {
	counter++;
	console.log("Counter: " + counter);

	if(counter == 3)
		clearInterval(id);
}
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija JavaScript]]
Nākama lapa >>> [[Taimeri]]

---