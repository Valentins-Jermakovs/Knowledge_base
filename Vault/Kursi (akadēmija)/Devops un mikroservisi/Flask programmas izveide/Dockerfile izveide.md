___

**Datums:** 2025-09-27
**Laiks:** 15:53
❚ **Tagi:** #devops 

---
# Dockerfile izveide

Šo failu parasti veido projekta saknē, nekādos apakškatalogos to neliek.

```python
# Uzliekam Python versiju un Linux distributīvu,
# uz kura darbosies konteineris
FROM python:3.11-alpine

# Izveidojam saknes katalogu programmai
WORKDIR /app

# Kopējam dependecy (pieprasīto bibliotēku failu) konteinera failu sistēmā
# direktorijā app
COPY ./requirements.txt /app/requirements.txt

# Šī komanda instalē visu nepieciešamo mūsu programmai
RUN pip install -r requirements.txt

# Šī komanda kopē visus projekta failus
# uz konteinera saknes (/app) katalogu
COPY . /app

# Šī programma darbina programmu konteinerī
ENTRYPOINT ["python"]
# Uzliek Entry point parametrus, lai izpildīt šo komandu
# analoģisks python app.py
CMD ["app.py"]
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[requirements.txt faila izveide]]
Nākama lapa >>> [[Kursi (akadēmija)/Devops un mikroservisi/Flask programmas izveide/Programmas konteinerizācija]]

---