___

**Datums:** 2025-09-27
**Laiks:** 15:32
❚ **Tagi:** #devops 

---
# Projekta izveide (bibliotēku instalācija)

Nepieciešams sainstalēt šādas bibliotēkas:

```bash
pip install Flask
pip install mysql-connector-python
```

Pēc tam pašā projektā importē šādas bibliotēkas:

```python
from flask import Flask, render_template
import mysql.connector
import json
```

Lai vairāk izprast `Flask` freimvorku, ieteicams apskatīt šo lapu >>>
[Создание Web-приложения Flask и деплой с помощью Docker Compose & Dockerfile](https://python.ivan-shamaev.ru/run-install-deploy-flask-web-app-docker-dockerfile-compose/)

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[venv izveidošana]]
Nākama lapa >>> [[Projekta pieslēgšana pie DB]]

---