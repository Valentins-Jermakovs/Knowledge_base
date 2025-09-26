___

**Datums:** 2025-08-11
**Laiks:** 19:24
❚ **Tagi:** #css 
⌬ **Priekšmets:**  `CSS`

---
### ⬢ Detalizēts apraksts
#### Pozicionēšana

![[Pasted image 20250811192918.png]]

| Vērtība                    | Apraksts                                                                                               | Īpašības                                                                                                                                |
| -------------------------- | ------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------- |
| **static** _(noklusējuma)_ | Elements seko parastajai lapas plūsmai                                                                 | `top`, `left`, `right`, `bottom` neietekmē                                                                                              |
| **relative**               | Novietots attiecībā pret savu parasto pozīciju                                                         | Var pārbīdīt ar `top`, `left`, `right`, `bottom`; citi elementi savu pozīciju nemaina                                                   |
| **absolute**               | Novietots attiecībā pret tuvāko **pozicionēto** priekšteci (`relative`, `absolute`, `sticky`, `fixed`) | Ja nav priekšteča — pret `body`; izņemts no plūsmas, var pārklāt citus elementus                                                        |
| **fixed**                  | Novietots attiecībā pret **viewport** (redzamo ekrāna daļu)                                            | Nemainās, ritinot lapu; izņemts no plūsmas                                                                                              |
| **sticky**                 | Kombinācija no `relative` un `fixed`                                                                   | Līdz noteiktam ritināšanas punktam ir `relative`, tad “pielīp” (`fixed`); nepieciešams vismaz viens no `top`, `left`, `right`, `bottom` |

```css
/* Relatīvs elements */
div.relative {
  position: relative;
  left: 20px;
}

/* Absolūts elements */
div.absolute {
  position: absolute;
  top: 10px;
  right: 0;
}

/* Fiksēts elements */
div.fixed {
  position: fixed;
  bottom: 0;
  right: 0;
}

/* “Līpošs” elements */
div.sticky {
  position: sticky;
  top: 0;
}
```

---
### ⇄ Saistības

Avots >>> [CSS Layout - The position Property](https://www.w3schools.com/css/css_positioning.asp)
Iepriekšēja lapa >>> [[Tabulas]]
Nākama lapa >>> [[z-index]]

---