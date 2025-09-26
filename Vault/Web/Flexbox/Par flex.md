___

**Datums:** 2025-08-11
**Laiks:** 14:20
❚ **Tagi:** #css #flexbox 
⌬ **Priekšmets:**  `Flexbox`

---
### ⬢ Detalizēts apraksts
#### `flex` īpašība

Šī īpašība ļauj kontrolēt to, kā `flex` konteinera elementi uzvedīsis atkarībā no izmēra maiņas.

`flex` ir īsa forma šim 3 īpašībām:

- `flex-grow` - atbilst par to, kā augs elementi, ja konteineri palielināt, cik reizes paliks lielāks;
- `flex-shrink` - atbilst par to, kā samazināsies elementi, ja konteineri samazināt, cik reizes paliks mazāks;
- `flex-basis` - iestata pamata izmēru/platumu elementam, parasti pikseļos vai procentos, noklusējuma platums.

```
flex: 1 ir tas pats, kā:

flex-grow: 1;
flex-shrink: 1;
flex-basis: 0;

un tas pats, kā:
flex: 1 1 0;
```

`flex` var pieņemt 3 parametrus, kur tu iestati katru manuāli, a vai vienu.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Par align-self]]
Nākama lapa >>> [[Par flex-wrap]]

---