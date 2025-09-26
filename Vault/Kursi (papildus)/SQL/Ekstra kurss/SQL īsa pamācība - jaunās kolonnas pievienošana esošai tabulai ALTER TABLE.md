___

**Datums:** 2025-08-04   
**Laiks:** 11:26 

❚ **Tagi:** #SQL 
⌬ **Priekšmets:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Jaunās kolonnas pievienošana tabulai

Dažreiz ir situācijas, kad tabula jau izveidota, taču nepieciešams pievienot jauno kolonnu. Šādās situācijās izmanto `ALTER TABLE`.

Sintakse:

```sql
ALTER TABLE tabulas_nosaukums ADD jaunās_kolonnas_nos juanās_kolonnas_datu_tips
```


> [!NOTE] Atgādinājums
> Jaunās kolonnas lauki automātiski tiks aizpildīti ar `NULL` vērtībām. Lai šo situāciju labot, izmanto operatoru `UPDATE`, kas aprakstīts nākamā nodaļā.


---
### ⇄ Saistības

Iepriekšēja lapa >>> [[SQL īsa pamācība - datu šķirošana ORDER BY]]
Nākama lapa >>> [[SQL īsa pamācība - datu atjaunošana, ierakstīšana UPDATE]]

___