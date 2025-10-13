___

**Datums:** 2025-10-13
**Laiks:** 14:33
❚ **Tagi:** #kotlin

---
# fold() funkcija

Šī funkcija tiek izmantota, lai uzģenērt vienu vērtību balstoties uz visas kolekcijas vērtībām:

```kotlin
val totalPrice = cookies.fold(0.0) {total, cookie ->
    total + cookie.price
}
```

- `0.0` ir sākuma vērtība;
- `total` - mainīgais, kurā tiek ierakstīta summa;
- `cookie` - ir `cookies` kolekcijas elements.

Pēc `->` tiek aprasktīt izpildāmais kods.

```kotlin
println("Total price: $${totalPrice}")
// Total price: $10.83
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[groupBy funkcija]]
Nākama lapa >>> [[sortedBy funkcija]]

---