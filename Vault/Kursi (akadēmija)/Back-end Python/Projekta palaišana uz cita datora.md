___

**Datums:** 2025-10-08
**Laiks:** 15:48
❚ **Tagi:** #back-end #python 

---
# Projekta apalaišana uz cita datora 

Šī instrukcija darbojas tikai, ja esi izveidojis failu `requirements.txt` un izmanto `LiteSQL`.

Lai palaist `Django` projektu uzcita datora, veic šādas darbības:

1. `conda create -n myprojectenv python=3.11` - izveido jauno virtuālo mašīnu;
2. `conda activate myprojectenv` - aktivizē to;
3. pārēj uz projekta katalogu;
4. `pip install -r requirements.txt` - palaid šo skriptu, lai instalēt visas nepieciešamas bibliotekas. Ja dažas bibliotēkas neisntalējas, liec tās caur `conda install`;
5. `python manage.py migrate` - veic migrācijas;
6. `python manage.py runserver` - palaid severi.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - back-end python]]

---