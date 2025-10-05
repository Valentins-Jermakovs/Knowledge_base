___

**Datums:** 2025-09-22
**Laiks:** 19:32
❚ **Tagi:** #back-end #python 

---
# Ceļa izveidošana

Pirmkārt, pārēj uz failu `url.py`. Tur veic faila `view.py` importu.

```python
# Importe dispetcera funkcijas - fails, kas apstrada pieprasijumus
from .views import *
```

`*` - visas funkcijas. Tu vari arī manuāli importēt tikai noteiktas funkcijas, norādot to nosaukumu.

Pēc tam pievērs uzmanību masīvam `urlpatterns`. Šis masīvs satur ceļus un tiem piesaistitas funkcijas (skatus).

```python
urlpatterns = [
    # Noklusejuma cels un funkcija
    path("", dynamic_page),         # manis definēts ceļš
    path("pageOne", page_one_view), # manis definēts ceļš
    path("pageTwo", main_view),     # manis definēts ceļš
    path('admin/', admin.site.urls),
]
```

Lai izveidot ceļu, izmanto šādu sintaksi:

```
path("/ceļš", skats),
```

*Autora piezīmes:*

Ceļš var saturēt vairākus `/` simbolus. Skats ir tevis veidota funkcija.

Šādi izskatās viss `url.py` fails:

```python
"""
URL configuration for myApp project.

The `urlpatterns` list routes URLs to views. For more information please see:
    https://docs.djangoproject.com/en/5.2/topics/http/urls/
Examples:
Function views
    1. Add an import:  from my_app import views
    2. Add a URL to urlpatterns:  path('', views.home, name='home')
Class-based views
    3. Add an import:  from other_app.views import Home
    4. Add a URL to urlpatterns:  path('', Home.as_view(), name='home')
Including another URLconf
    5. Import the include() function: from django.urls import include, path
    6. Add a URL to urlpatterns:  path('blog/', include('blog.urls'))
"""
from django.contrib import admin
from django.urls import path

# Importe dispetcera funkcijas - fails, kas apstrada pieprasijumus
from .views import *

urlpatterns = [
    # Noklusejuma cels un funkcija
    path("", dynamic_page),
    path("pageOne", page_one_view),
    path("pageTwo", main_view),
    path('admin/', admin.site.urls),
]
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Skatu izveide]]
Nākama lapa >>> [[Moduļa izveide]]

---