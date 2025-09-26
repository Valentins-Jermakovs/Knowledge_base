___

**Datums:** 2025-08-19
**Laiks:** 16:53
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### KeyboardEvent

Tastarūras notikumu tabula:

| Notikums     | Apraksts                                                                                         | Notikuma objekts |
| ------------ | ------------------------------------------------------------------------------------------------ | ---------------- |
| **keydown**  | rodas, kad tiek nospiesta tastatūras taustiņš, un notikums turpinās, kamēr taustiņš ir nospiests | KeyboardEvent    |
| **keyup**    | rodas, kad tastatūras taustiņš tiek atlaists                                                     | KeyboardEvent    |
| **keypress** | rodas, kad tiek nospiests tastatūras taustiņš, bet pēc _keydown_ un pirms _keyup_ notikuma       | KeyboardEvent    |

Lai strādātu ar tastatūras notikumiem, tiek definēts KeyboardEvent objekts, kas Event objekta īpašībām pievieno vairākas tastatūrai specifiskas īpašības:

- **altKey**: atgriež _true_, ja notikuma ģenerēšanas laikā bija nospiests taustiņš **Alt**
- **key**: atgriež nospiestā taustiņa simbolu.  
    Piemēram, ja nospiests taustiņš **"T"**, īpašība saturēs `"T"`. Ja nospiests taustiņš **"Я"**, īpašība saturēs `"Я"`.
- **code**: atgriež nospiestā fiziskās tastatūras taustiņa QWERTY kodu virknes formā.
    - Piemēram, ja nospiests taustiņš **"T"**, īpašība saturēs `"KeyT"`.
    - Ja nospiests taustiņš **";"**, īpašība saturēs `"Semicolon"`.
    
    👉 Ņem vērā:
    1. Tiek izmantots **QWERTY izkārtojums** neatkarīgi no aktīvās valodas. Piemēram, ja ir ieslēgta krievu izkārtojuma tastatūra un tiek nospiests taustiņš **"Я"**, vērtība būs `"KeyZ"`, jo QWERTY tastatūrā tā pati poga atbilst burtam **Z**.
    2. Tiek ņemta vērā tieši **fiziskā tastatūra**. Ja tiek izmantota virtuālā tastatūra, pārlūks pats nosaka atbilstošo kodu atkarībā no tā, kuram fiziskās tastatūras taustiņam atbilst nospiešana.

- **ctrlKey**: atgriež _true_, ja notikuma ģenerēšanas laikā bija nospiests taustiņš **Ctrl**
- **metaKey**: atgriež _true_, ja notikuma ģenerēšanas laikā bija nospiests tastatūras **Meta** taustiņš (piemēram, **Command** uz Mac)
- **shiftKey**: atgriež _true_, ja notikuma ģenerēšanas laikā bija nospiests taustiņš **Shift**.

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
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
const blueRect = document.getElementById("blueRect");
// получаем стиль для blueRect
const blueRectStyle = window.getComputedStyle(blueRect);
// устанавливаем обработчик нажатия клавиши
window.addEventListener("keydown", moveRect);
 
function moveRect(e){
    const left = parseInt(blueRectStyle.marginLeft); //смещение от левого края
    const top = parseInt(blueRectStyle.marginTop);  // смещения от левой границы
     
    switch(e.key){
         
        case "ArrowLeft":  // если нажата клавиша влево
            if(left>0)
                blueRect.style.marginLeft = left - 10 + "px";
            break;
        case "ArrowUp":   // если нажата клавиша вверх
            if(top>0)
                blueRect.style.marginTop = top - 10 + "px";
            break;
        case "ArrowRight":   // если нажата клавиша вправо
            if(left < document.documentElement.clientWidth - 100)
                blueRect.style.marginLeft = left + 10 + "px";
            break;
        case "ArrowDown":   // если нажата клавиша вниз
            if(top < document.documentElement.clientHeight - 100)
                blueRect.style.marginTop = top + 10 + "px";
            break;
    }
}
</script>
</body>
</html>
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| События клавиатуры](https://metanit.com/web/javascript/9.6.php)
Iepriekšēja lapa >>> [[MouseEvent]]
Nākama lapa >>> [[Navigācija JavaScript]]

---