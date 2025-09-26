___

**Datums:** 2025-08-30
**Laiks:** 13:52
❚ **Tagi:** #javascript 

---
### Ievads

Katram pārlūkam ir iekšēja krātuve (storage), kurā var glabāt nelielu datu apjomu. 

Šī glabātuve sastāv no 2 komponentēm:

- `session storage` - datu krātuve, kas saglabā datus līdz pārluka loga izslēgšanai;
- `local storage` - lokāla pārlūka krātuve, kas saglabā datus lokāli uz lietotāja ierīces. Dati netiek automātiski dzēsti vai nosūtīti uz serveri. Šādas krātuves apjoms ir 5 megabaiti.

Visi dati `web-storage` ir `key-value` vērtības. Katram objektam ir sava unikāla atslēga un vērtība.

Darbam ar `local storage` tiek izmantots objekts `localStorage`.
Darbam ar `session storage` tiek izmantots objekts `sessionStorage`.

Abiem objektiem ir vienādas metodes:

| Metode              | Ko dara?                                                                                                                       |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| length              | Satur elementu daudzumu krātuvē.                                                                                               |
| clear()             | Izdzēš visus elementus no krātuves.                                                                                            |
| getItem(key)        | Atgriež konkrētu vērtību pēc norādītas atslēgas (key).                                                                         |
| key(index)          | Atgriež elementa atslēgu pēc norādītas vērtības (index).                                                                       |
| removeItem(key)     | Izdēš elementu pēc norādītas atslēgas (key).                                                                                   |
| setItem(key, value) | Uzliek elementam `key` un `value`. Ja elements ar šādu `key` jau eksistē krātuvē, tas tiek pārrakstīts, ja nē, tad pievienots. |

---
### ⇄ Saistības

Avots >>> [JavaScript \| Web Storage](https://metanit.com/web/javascript/12.2.php)
Iepriekšēja lapa >>> [[Navigācija Web-storage]]
Nākama lapa >>> [[Datu saglabāšana]]

---