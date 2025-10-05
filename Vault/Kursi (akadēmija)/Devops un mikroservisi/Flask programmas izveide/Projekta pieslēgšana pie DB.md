___

**Datums:** 2025-09-27
**Laiks:** 15:38
❚ **Tagi:** #devops 

---
# Projekta pieslēgšana pie DB

Piemērs, kā izveidot pieslēgu pie DB, kas izvietota konteinerī:

```python
# Funkcija atgriež tabulas ierakstus un JSON dokumentu
def get_missions():

    # Savienojuma izveide ar DB
    # Izveidojam vārdnīcu ar nepieciešamiem datiem,
    # lai varētu veiksmīgi pieslēgties pie DB
    config = {
        'host': 'mysql1',                # Servera nosaukums
        'user': 'root',                  # Lietotāja vārds
        'password': 'root123',           # Parole
        'database': 'myDB',              # DB nosaukums
        'port': 3306                     # Atvērta porta numurs
    }

    # Veidojam savienojuma objektu
    cnx = mysql.connector.connect(**config)

    # Veicam pārbaudi uz savienojma esamību
    if cnx and cnx.is_connected():

        # Izveidojam kursoru, kas veic SQL pieprasījumus
        # dictionary=True nozīmē, kā vaicājuma rezultāts būs vārdnīca, nevis kortežs
        #
        # with ir konteksta menedžeris, kas aizvērs savienojumu automātiski,
        # ja tās neizdosies

        with cnx.cursor(dictionary=True) as cursor: 

            # Šeit tiek veikts SQL pieprasījums
            cursor.execute("SELECT * FROM space_missions")
            # Paņemam visu pieprasījuma rezultātu
            rows = cursor.fetchall()

            # Konvertējam uz JSON dokumentu
            # default=str nepieciešams, 
            # lai konvertēt datetime datu tipu uz string
            data = json.dumps(rows, default=str)
    
    # Ja savienojumu neizdevās izveidot
    else:
        # Tukšie dati
        rows = []           # Tabulas ieraksti
        data = "Not data!"  # Dokuments

    
    cnx.close()         # Aizveram savienojumu ar DB
    return [rows, data] # Atgriežam datus masīvā
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Projekta izveide (bibliotēku instalācija)]]
Nākama lapa >>> [[Kursi (akadēmija)/Devops un mikroservisi/Flask programmas izveide/Šablona izveide]]

---