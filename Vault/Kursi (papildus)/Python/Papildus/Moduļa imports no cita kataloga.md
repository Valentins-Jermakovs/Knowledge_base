___

**Datums:** 2025-08-03   
**Laiks:** 15:18 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Moduļi no citiem katalogiem

##### Variants 1: Relatīvais ceļš izmantojot `sys.path`

Ja struktūra direktorijām ir, piemēram:

```
projekts/
├── main.py
└── utilites/
    └── pizza.py
```

Tad `main.py`:

```python
import sys
sys.path.append('./utilites')  # pievieno ceļu uz moduļa direktoriju

import pizza

pizza.make_pizza(16, 'pepperoni')
```

##### Variants 2: Absolūtais ceļš, ja projekts ir strukturēts kā Python pakotne

Struktūra:

```
projekts/
├── main.py
└── utilites/
    ├── __init__.py
    └── pizza.py
```

Tad `main.py`:

```python
from utilites import pizza

pizza.make_pizza(16, 'pepperoni')
```

Ja neizdodas importēt, pārliecinies, ka:

- Ir `__init__.py` fails direktorijā (pat ja tukšs) <mark style="background: #FF5582A6;">šis fails ir obligāts!</mark>.
- Palaid skriptu no **saknes**, t.i. no `projekts/`, lai Python zinātu, kur meklēt moduli.

##### Rekomendējama projekta struktūra

```
projekts/
├── main.py
├── utilites/
│   ├── __init__.py
│   └── pizza.py
├── models/
│   ├── __init__.py
│   └── ingredients.py
└── README.md
```

`main.py`

```python
from utilites.pizza import make_pizza
from models.ingredients import dough
```

##### `__init__.py`

###### Tukšais fails

> Fails `__init__.py` vajadzīgs, lai varetu importēt moduļus no apakškatalogiem. Tas var būt kā tukšs, tā arī kaut ko saturēt sevī.

```python
# __init__.py (tukšs fails)
```

###### Autmomātisks imports, piem., ja gribi, lai pēc importa būtu pieejamas visas funkcijas:

```python
# utilites/__init__.py

from .pizza import make_pizza, make_calzone
```

Failā `main.py` tagad vari darīt šādi:

```python
from utilites import make_pizza
```

###### Inicializācijas kods

```python
# utilites/__init__.py

print("Импортирован пакет utilites")

__version__ = "1.0.0"
__all__ = ["make_pizza", "make_calzone"]

from .pizza import make_pizza, make_calzone
```

`__all__ `ierobežo to, kas tiek importēts `from utilites import *`

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Sevis veidota moduļa (faila) imports]]
Nākama lapa >>> [[Navigācija - Python strukturēts]]

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Sevis veidota moduļa (faila) imports]]
Nākama lapa >>> [[Navigācija - Python]]

___