___

**Datums:** 2025-09-27
**Laiks:** 15:45
❚ **Tagi:** #devops 

---
# Šablona izveide

Šabloni ir gana līdzīgi tam, ko izmanto `django` freimvorks.

Pašā projektā ir funkcijas, kas atgriež skatus. Piemērā tiek izsaukts `my_page_view.html`, kuram programma nodod datus:

```python
# Dekorators + Funkcija
@app.route('/') # Dekorators - skats (adrese)
def render_my_data():    # Funkcija, kas atgriež skatu (renderē šablonu un nodod datus)

    user_name = 'Valentīns'        # Iestatam mainīgo - name

    # Šeit tiek iegūti dati no DB
    big_data = get_missions()       # Saglabājam funkcijas rezultātu
    missions = big_data[0]          # Iegūstam misiju sarakstu
    missions_json = big_data[1]     # Iegūstam JSON dokumentu

    # Šis tiek atgriezts skatā, kā arī renderēts
    return render_template(
        'my_page_view.html',        # HTML šablons
        name = user_name,           # 1. mainīgais
        missions = missions,        # 2. mainīgais
        data = missions_json        # 3. mainīgais
        )
```

Šādi izskatās pats šablons, konkrēti tiks izceltas vietas, kur tiek izmantoti šādi te mainīgie:

```html
<h1 class="text-4xl font-extrabold text-blue-600 mb-2">Sveiks, {{ name }}!</h1>
```

Šajā piemērā tiek sagaidīts mainīgais `name`.

```html
<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
            {% for mission in missions %}
            <div class="bg-white p-4 rounded-lg shadow hover:shadow-lg transition duration-300">
                <h3 class="text-xl font-bold text-blue-600 mb-2">{{ mission.name }}</h3>
                <p><strong>Agency:</strong> {{ mission.agency }}</p>
                <p><strong>Launch Date:</strong> {{ mission.launch_date }}</p>
                <p><strong>Mission Type:</strong> {{ mission.mission_type }}</p>
                <p><strong>Destination:</strong> {{ mission.destination }}</p>
            </div>
            {% endfor %}
        </div>
```

Šeit jau tiek veidots vesels cikls. `{% for mission in missions %}` norāda, kā tiek sagaidīts masīvs, mūsu gadījumā tas ir masīvs ar vārdnīcām. `{% endfor %}` ir nobeigums. Šādi var renderēt masīvus.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Projekta pieslēgšana pie DB]]
Nākama lapa >>> [[requirements.txt faila izveide]]

---