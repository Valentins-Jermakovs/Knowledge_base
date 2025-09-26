___

**Datums:** 2025-09-22
**Laiks:** 18:55
❚ **Tagi:** #back-end #python 

---
# Skatu izveide

Pirms skata veidošanas nepieciešams pats projekts, ko var izveidot apskatoties iepriekšējo instrukciju.

Neliela instrukcija, lai palaist pašu projektu:

1. aktivizēt virtuālo mašīnu;
2. pāriet projekta katalogā:
	1. iekopēt ceļu no *file explorer*;
	2. `cd .../ceļš līdz projektam`;
3. palaist serveri:
	1. `python manage.py runserver`.

Lai izveidot pašu skatu:

1. izveodto projektā failu `views.py`;
2. pieslēgt `HttpResponse`.

Zemāk ir koda paraugs failam `views.py`:

```python
# Šeit tiek izvietotas funkcijas,
# kas apstrāda pieprasījumus

# importē priekš response
from django.http import HttpResponse

# Funkcijam obligāts parametrs - request
# Visiem skatiem beigās return, tas ir obligāts!

def main_view(request):
    return HttpResponse("Hello World!")

def page_one_view(request):
    return HttpResponse("<div style='color:red'>Hello Creator!</div>")

def function_three(request):
    return HttpResponse("<h1>Sveiki! 1. septembris Oh my God, not again...<h1>")

# Mana lapa ar loģiku
# Lapa, kas veido tekstu dinamiski - izvada lokālo sistēmas laiku                                         
import datetime # importe datetime - priekš laika nolasīšanas
def dynamic_page(request):
    time = get_time()
    return HttpResponse(time)

# Funkcija, kas iegust lokalo laiku
def get_time():
    time = str(datetime.datetime.now())
    return time
```

*Autora piezīmes.*

Skatu nosaukumu definēšanas piemēri (labā prakse):

- main_view;
- style_demo_view;
- poage_demo_view.

```
'<div style="color:red">Hello world!</div>'
```

Ieteikums: ievieto pašu `HTML` atgriežamo objektu `single` pēdiņās, paša stila aprakstu dubultās.

Skats ir funkcija, kas atgriež `HTML` kodu ar/bez stiliem.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Jaunā projekta izveide]]
Nākama lapa >>> [[Skata pieslēgšana, ceļa izveide]]

---