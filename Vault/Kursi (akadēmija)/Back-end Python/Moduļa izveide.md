___

**Datums:** 2025-10-05
**Laiks:** 14:13
❚ **Tagi:** #back-end #python 

---
# Moduļa izveide

## Moduļa pieslēgšana pie projekta

Lai izveidot moduli, jāveic šādus soļus:

**Pirmkārt**, jāizpilda šāda komanda:

```
python manage.py startapp moduļa_nosaukums
```

Šī komanda izveido moduļa katalogu ar visiem nepieciešamiem failiem automātiski.

**Otrkārt**, jāpieslēdz modulis pie paša projekta. Nepieciešams atvērt galvenās programmas katalogu, piem., `my_project` un jāpariet uz failu `settings.py`. Šajā failā veic norādītas modifikācijas:

```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    # Pievienoju savus moduļus
    'zenergy.apps.ZenergyConfig',
]
```

`ZenergyConfig` - šo te funkciju vari atrast sava moduļa `apps.py` failā, tā tiek ģenerēta automātiski.

## Skata veidošana modulī

Lai izveidot skatu savam jaunajam modulim, moduļa failā `views.py` veic šādas modifikācijas:

```python
# Importē bibliotēku
from django.http import HttpRespone

# Izveido funkciju, kas atgriež skatu
def cart_main_view(request):
	return HttpResponse('<h1>Cart</h1>')
```

Pēc šādas modifikācijas, nepieciešams pieslēgt skatu pie maršrutiem, galvenās programmas fails `urls.py`:

```python
# Importē skatus veidojošas funkcijas
from cart.vies import *
# Pieslēdz skatu masīvā
urlpatterns = [
	path('cart', cart_main_view),
	...
]
```

## Moduļa maršrutu veidošana (apakšmaršruti)

Savā modulī izveido failu `urls.py`. Paņem visu no galvenās programmas `urls.py` faila un iekopē, ielīmē saturu, izdzēs lieko. Šeit vari apskatīt mana projekta paraugu:

```python
# Šis fails tiek izmantots, lai definētu URL maršrutus zenergy lietotnei.
from django.contrib import admin
from django.urls import path

# Importējam skatus no šī moduļa
from .views import *

urlpatterns = [
    # Zenergy maršrutu saraksts
    path("", zenergy_home_view, name="zenergy-home"),                           # /zenergy (home page)
    path("electricity/", zenergy_electricity_view, name="zenergy-electricity"), # /zenergy/electricity (apkopo datus par ražošanu)
    path("electricity-prices/", zenergy_electricity_prices_view, name="zenergy-electricity-prices"), # /zenergy/electricity/prices
    path("co2/", zenergy_co2_view, name="zenergy-co2"),                         # /zenergy/co2
    path("calendar/", zenergy_calendar_view, name="zenergy-calendar"),          # /zenergy/calendar
]
```

Pēc tam mums nepieciešams galvenās programmas failā `urls.py` importēt visus moduļa maršrutus:

```python
# Importēju nepieciešamas bibliotēkas (OBLIGĀTI)
from django.urls import include

urlpatterns = [
    path('admin/', admin.site.urls),
    # Importēju sava moduļa maršrutus
    path("", include("zenergy.urls")),
]
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Skata pieslēgšana, ceļa izveide]]
Nākama lapa >>> [[Kursi (akadēmija)/Back-end Python/Šablona izveide|Šablona izveide]]

---