___

**Datums:** 2025-08-09
**Laiks:** 15:29
❚ **Tagi:** #css
⌬ **Priekšmets:**  `CSS`

---
### ⬢ Detalizēts apraksts
#### Par `background-image`

Šī īpašība ļauj uzlikt fona attēļu elementam.

```css
.container {
	background-image: url('ceļš_līdz failam');
}
```

Papildus ar to ieteicams izmantot `background-size`. Tas nosaka izmēru `background-image`.

Vērtību tabula `background-size`:

| Vērtība      | Apraksts                                                                                                                                                                                    |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `auto`       | Noklusējuma vērtība. Fona attēls tiek parādīts tā sākotnējā izmērā                                                                                                                          |
| `length`     | Nosaka fona attēla platumu un augstumu. Pirmais parametrs nosaka platumu, otrais – augstumu. Ja ir norādīta tikai viena vērtība, otrā tiek iestatīta uz `"auto"`.                           |
| `percentage` | Nosaka fona attēla platumu un augstumu procentos no vecākelementa. Pirmais parametrs nosaka platumu, otrais – augstumu. Ja ir norādīta tikai viena vērtība, otrā tiek iestatīta uz `"auto"` |
| `cover`      | Maina fona attēla izmēru tā, lai tas nosegtu visu konteineru, pat ja nepieciešams izstiept attēlu vai nogriezt nelielu daļu no malas                                                        |
| `contain`    | Maina fona attēla izmēru tā, lai tas būtu pilnībā redzams                                                                                                                                   |

```css
#example1 {
  background: url(img_tree.gif), url(mountain.jpg);
  background-repeat: no-repeat;
  background-size: contain, cover;
}
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Navigācija - HTML un CSS (2. daļa) strukturēts saturs]]
Nākama lapa >>> [[Gradients]]

---
### ⇄ Saistības

Avots >>> [CSS background-size property](https://www.w3schools.com/cssref/css3_pr_background-size.php)
Iepriekšēja lapa >>> [[margin shorthand (īsa pieraksta forma)]]
Nākama lapa >>> [[Google fonti]]

---