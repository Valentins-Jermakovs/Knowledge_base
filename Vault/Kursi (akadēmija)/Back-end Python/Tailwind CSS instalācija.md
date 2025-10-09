___

**Datums:** 2025-10-09
**Laiks:** 19:23
❚ **Tagi:** #back-end #python 

---
# Tailwind CSS instalācija

Links uz instrukciju >>> [Installation — Django-Tailwind 2.0.0 documentation](https://django-tailwind.readthedocs.io/en/latest/installation.html)

Soļi, kas jāveic lai instalēt `tailwind`:

1. `python -m pip install django-tailwind`
2. Add `'tailwind'` to `INSTALLED_APPS` in `settings.py`:
```
INSTALLED_APPS = [
  # other Django apps
  'tailwind',
]
```
3. Create a _Tailwind CSS_ compatible _Django_ app, I like to call it `theme`:
```
python manage.py tailwind init
```
4. Add your newly created `'theme'` app to `INSTALLED_APPS` in `settings.py`:
```
INSTALLED_APPS = [
  # other Django apps
  'tailwind',
  'theme'
]
```
5. Register the generated `'theme'` app by adding the following line to `settings.py`:
```
TAILWIND_APP_NAME = 'theme'
```
6. Install _Tailwind CSS_ dependencies by running the following command:
```
python manage.py tailwind install
```
7. Komanda, lai palaist projektu: `python manage.py tailwind dev`

Piemērs, kā pieslēgt `tailwind` no `theme` kataloga pie kāda cita moduļa šablona:

![[Pasted image 20251009192836.png]]

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Lekcijas konspekts 1]]
Nākama lapa >>> [[šablons]]

---