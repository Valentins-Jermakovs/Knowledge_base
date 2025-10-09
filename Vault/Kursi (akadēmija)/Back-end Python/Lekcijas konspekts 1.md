___

**Datums:** 2025-10-09
**Laiks:** 19:01
❚ **Tagi:** #back-end #python 

---
# Lekcijas konspekts 1

Šādi var atgriezt skatu, jauns veids:

```python
# Galvenais skats - zenergy_home_view
def zenergy_home_view(request):
    # Mainīgo bloks
    content = {}
    # Atgriežam šablonu un mainīgos
    return render(request, 'home_page_content.html', content)
```

Šādi var pieslēgt vairākas šablonu mapes, norādot caur komatu. Šeit `os` importēt nevajag:

![[celu pieslegsana.png]]

Katram modulim veido savu `static` mapi, tā saturēs `css, images un javascript` failus.

Mapes `static` veidošanas labā prakse:

`my_app/static/my_app/css/styles.css`

Šāda veidošana atcels vienādu failu nosaukumu kļūdas.

Lai pieslēgt šo lietu pie sava moduļa, galvenē liec tagu `{% load static %}`.
Pie `<head>` pievieno šo kodu:

```html
<link rel="stylesheet" href="{% static 'zenergy/images/hello.jpg' %}">
```

Lai labāk izsprast ieteicams papraktizēties.

![[Pasted image 20251009191737.png]]

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Kursi (akadēmija)/Back-end Python/Mantošana|Mantošana]]
Nākama lapa >>> [[Tailwind CSS instalācija]]

---