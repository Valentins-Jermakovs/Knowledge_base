___

**Datums:** 2025-08-15
**Laiks:** 20:59
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Apakšrindas izvēle

Lai izgriezt no teksta virknes apakšrindu, izmanto metodes:

- `substring()`
- `slice()`

##### Metode `substring()`

Metode pieņem 2 parametrus:

```
substring(startIndex, endIndex)
```

- `startIndex` - obligāts parametrs, sākuma indekss, no kura sākas griezums;
- `endIndex` - indekss, līdz kuram tiek veikts griezums. Ja to nenorāda, iet līdz teksta virknes beigām.

```js
const hello = "привет мир. пока мир";
const world = hello.substring(7, 10); // с 7-го по 10-й индекс
console.log(world); // мир
const bye = hello.substring(12);    // c 12 индекса до конца строки
console.log(bye); // пока мир
```

##### Metode `slice`

Metode arī pieņem 2 parametrus:

```
slice(startIndex, endIndex)
```

- `startIndex` - obligāts parametrs, sākuma indekss, no kura sākas griezums;
- `endIndex` - indekss, līdz kuram tiek veikts griezums. Ja to nenorāda, iet līdz teksta virknes beigām.

Atšķirība no iepriekšējas metodes tāda, kā `slice` ļauj izmantot negatīvus indeksus:

```js
const hello = "привет мир. пока мир";
const bye1 = hello.slice(-8, -4); // с 8-го индекса с конца до 4 индекса с конца
console.log(bye1); // пока
const bye2 = hello.substring(-8, -4); // не работает
console.log(bye2); // 
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Строки](https://metanit.com/web/javascript/6.1.php)
Iepriekšēja lapa >>> [[Meklēšana teksta virknē]]
Nākama lapa >>> [[Reģistra maiņa]]

---