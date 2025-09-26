___

**Datums:** 2025-08-03   
**Laiks:** 15:07 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Moduļa imports

##### Visa moduļa imports

Jāizveido fails, piem., `pizza.py`, tādā pašā katalogā, kur atrodas pamata programmas fails.
Pēc tam, galvenajā failā:

```python
import pizza

pizza.make_pizza(16, pepperoni)
```
##### Konkrētas funkcijas importēšana

```python
# sintakse
from moduļa_nosaukums import funkcijas_nosaukums

# funkcijas pielietojums

make_pizza(16, pepperoni)
```

Ja vajag importēt vairākas funkcijas:

```python
from moduļa_nosaukums import funkcija_0, funkcija_1, funkcija_2
```

##### Pseidonīma izveidošana priekš funkcijas

```python
from pizza import make_pizza as mp

mp(16, pepperoni)
```

##### Pseidonīms visam modulim

```python
import pizza as p

p.make_pizza(16, pepperoni)
```

##### Visu funkciju importēšana

```python
# from moduļa nosaukums import *

from picca import *

make_pizza(16, pepperoni)
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Modulis re]]
Nākama lapa >>> [[Moduļa imports no cita kataloga]]

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[try...except konstrukcija]]
Nākama lapa >>> [[Moduļa imports no cita kataloga]]

___