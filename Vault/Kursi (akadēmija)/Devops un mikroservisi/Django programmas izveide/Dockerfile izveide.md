___

**Datums:** 2025-10-05
**Laiks:** 15:33
❚ **Tagi:** #devops 

---
# Dockerfile izveide

Šādi izskatās `Dockerfile` priekš `Django` programmas:

```python
# Virtuāla mašīna
FROM python:3.11-slim
# Tiek veidots saknes darba katalogs
WORKDIR /app
# Kopējam requirements failu
COPY requirements.txt .
# Instalējam requirements
RUN pip install -r requirements.txt
# Kopējam projekta failus
COPY . .

# Nosaka, kādu portu izmantot
EXPOSE 8000 
# Startējam projektu
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
```

Apmēram šādi tas izskatās, atšķirība no `flask` tāda, kā tiek norādīts noklusējuma porta numurs un veidots `CMD`.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[requirementstxt faila izveide]]
Nākama lapa >>> [[Kursi (akadēmija)/Devops un mikroservisi/Django programmas izveide/Programmas konteinerizācija|Programmas konteinerizācija]]

---