___

**Datums:** 2025-10-05
**Laiks:** 15:15
❚ **Tagi:** #back-end #python 

---
# Mantošana

Mantošanai tiek izmantoti šādi tagi:

- `{% extends paplašināna_šablona_nosaukums %}` - apraksta, kādu šablonu paplašina;
- `{% block bloka_nosaukums %}` - veidojam bloku, kas paplašina vecāka šablonu, kodu aprakstam pēc šī taga;
- `{% endblock %}` - beidzam aprakstīt bērna šablonu;
- `{% include %}` - ievietojam šablonu vecāka šablonā.

Šādi te izskatās vecāka šablons:

```django
<!DOCTYPE html>
<html lang="lv">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ZenPanelis</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
</head>

<body class="w-full min-h-screen bg-sky-100">

    <div class="grid grid-cols-1 xl:grid-cols-7 h-full xl:h-screen">
        <!-- Navigācija -->
        <div class="xl:col-span-1 xl:h-screen">
            {% include "navigation_panel.html" %}
        </div>

        <!-- Saturs -->
        <div class="xl:col-span-6 overflow-y-auto">
            <div class="w-full h-full flex flex-col items-center justify-between ">
                <!-- Statistikas saturs -->
                {% block electricity_window %}{% endblock %}
                <!-- Cenu kalendārs uz šodienu -->
                {% block electricity_prices %}{% endblock %}
                <!-- Footer --> 
                {% include "footer.html" %}
            </div>
        </div>
    </div>

</body>

</html>
```

Tags `{% include %}` ļauj ievietot komponenti pa taisno, tā tiek attēlota visās lapās.
Tagi `{% block electricity_prices %}{% endblock %}` veido tādu kā apakšlapu, lai tie būtu redzami, tos nepieciešāms renderēt atsevišķā skatā:

```python
# Elektrības cenu pārskāts uz rītdienu
def zenergy_electricity_prices_view(request):
    # Renders
    template = loader.get_template('prices_today.html')

    # Iegūstam datus - cenu grafiks
    data = ElectricityPrices()
    data = data.get_prices()

    # Iegūstam datus - lētākais un augstākais
    time_and_price = ElectricityHighestAndLowest()
    lowest = time_and_price.get_lowest_price()
    # Vismazākie rādītāji
    lowest_price = lowest[0]
    lowest_price_time = lowest[1]
    # Visaugstākie rādītāji
    highest_and_lowest = time_and_price.get_highest_price()
    highest_price = highest_and_lowest[0]
    highest_price_time = highest_and_lowest[1]
    # Iegūstam tagadējo laiku un cenu
    now_data = time_and_price.get_now_price()
    now_price = now_data[0]
    now_price_time = now_data[1]
    # Ierakstam visu vārdnīcā
    content = {
        "data" : data,
        "lowest_price" : lowest_price,
        "lowest_price_time" : lowest_price_time,
        "highest_price" : highest_price,
        "highest_price_time" : highest_price_time,
        "now_price" : now_price,
        "now_price_time" : now_price_time
    }

    return HttpResponse(template.render(content, request))
```

Un reģistrēt kā atsevišķo ceļu:

```python
urlpatterns = [

# Zenergy maršrutu saraksts

path("", zenergy_home_view, name="zenergy-home"), # /zenergy (home page)

path("electricity/", zenergy_electricity_view, name="zenergy-electricity"), # /zenergy/electricity (apkopo datus par ražošanu)

path("electricity-prices/", zenergy_electricity_prices_view, name="zenergy-electricity-prices"), # /zenergy/electricity/prices

path("co2/", zenergy_co2_view, name="zenergy-co2"), # /zenergy/co2

path("calendar/", zenergy_calendar_view, name="zenergy-calendar"), # /zenergy/calendar

]
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Django Template Language]]
Nākama lapa >>> [[Lekcijas konspekts 1]]

---