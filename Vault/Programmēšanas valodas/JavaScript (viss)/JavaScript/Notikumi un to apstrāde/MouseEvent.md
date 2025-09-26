___

**Datums:** 2025-08-19
**Laiks:** 16:35
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### MouseEvent

`Event` objekts ir kopīgs visiem notikumiem. Tomēr dažādiem notikumu veidiem ir arī notikumu objekti, kas pievieno vairākas savas īpašības. Tādējādi darbam ar peles rādītāja notikumiem ir definēts `MouseEvent` objekts, kas pievieno šādas īpašības:

- **altKey**: atgriež _true_, ja notikuma ģenerēšanas laikā bija nospiests taustiņš **Alt**;
- **button**: satur nospiestās peles pogas numuru;
- **buttons**: satur skaitli, kas attēlo nospiesto peles pogu:
    - `1` – kreisā poga,
    - `2` – labā poga,
    - `4` – rullītis vai vidējā poga,
    - `8` – ceturtā poga,
    - `16` – piektā poga.  
        Ja vienlaikus bija nospiestas vairākas pogas, šī īpašība satur atbilstošo skaitļu summu.
        
- **clientX**: nosaka X koordinātu pārlūka logā, kur notikuma laikā atradās peles rādītājs;
- **clientY**: nosaka Y koordinātu pārlūka logā, kur notikuma laikā atradās peles rādītājs;
- **ctrlKey**: atgriež _true_, ja notikuma ģenerēšanas laikā bija nospiests taustiņš **Ctrl**;
- **movementX**: satur X koordinātu nobīdi attiecībā pret iepriekšējo X koordinātu pēdējā peles kustības notikumā;
- **movementY**: satur Y koordinātu nobīdi attiecībā pret iepriekšējo Y koordinātu pēdējā peles kustības notikumā;
- **metaKey**: atgriež _true_, ja notikuma ģenerēšanas laikā bija nospiests tastatūras **Meta** taustiņš (piem., Command uz Mac);
- **region**: satur reģiona vai elementa identifikatoru, kas attiecas uz notikumu
- **relatedTarget**: nosaka sekundāro notikuma avotu;
- **screenX**: nosaka X koordinātu attiecībā pret ekrāna augšējo kreiso stūri, kur atradās peles rādītājs notikuma laikā;
- **screenY**: nosaka Y koordinātu attiecībā pret ekrāna augšējo kreiso stūri, kur atradās peles rādītājs notikuma laikā;
- **shiftKey**: atgriež _true_, ja notikuma ģenerēšanas laikā bija nospiests taustiņš **Shift**.

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <style>
    #blueRect{
        width:100px;
        height:100px;
        background-color:blue;
    }
    </style>
</head>
<body>
<div id="blueRect"></div>
 
<script>
function handleClick(e){
    console.log("screenX: " + e.screenX);
    console.log("screenY: " + e.screenY);
    console.log("clientX: " + e.clientX);
    console.log("clientY: " + e.clientY);
}
const blueRect = document.getElementById("blueRect");
blueRect.addEventListener("click", handleClick);
</script>
</body>
</html>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| События мыши](https://metanit.com/web/javascript/9.5.php)
Iepriekšēja lapa >>> [[Notikumu klausītāja pievienošana]]
Nākama lapa >>> [[MouseEvent]]

---