___

**Datums:** 2025-10-05
**Laiks:** 14:31
❚ **Tagi:** #back-end #python 

---
# Šablona izveide

Mūsu iepriekš veidotā modulī veidojam mapi `Templates`. Šeit mēs veidosim visus `HTML` dokumentus.

Pēc šablona izveides, to nepieciešams reģistrēt galvenās programmas failā `settings.py`:

```python
# Lai darbotos Templates
import os

TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        # Šeit importējam savu šablonu mapi pēc parauga
        'DIRS': [os.path.join(BASE_DIR, 'zenergy/templates')],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]
```

## Šablona renderēšana

Lai modulis varētu atgriezt/att elot mums nepieciešamo šablonu, failā `views.py` veicam šādas izmaiņas:

```python
# Pieslēdzam nepieciešamo bibliotēku
from django.template import loader

# Funkcija, kas atgriež skatu
def cart_main_view(request):
	# Iegūstam šablonu
	template = loader.get_template('cart_main.html')
	# Šablona mainīgie
	content = {}
	# Atgriežam šablonu ar visiem mainīgiem
	return HttpResponse(template.render(content, request))
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Moduļa izveide]]
Nākama lapa >>> [[Django Template Language]]

---