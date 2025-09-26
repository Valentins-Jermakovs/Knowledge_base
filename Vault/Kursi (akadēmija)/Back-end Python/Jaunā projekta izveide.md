___

**Datums:** 2025-09-12
**Laiks:** 13:46
❚ **Tagi:** #back-end #python 

---
### Darbību secība, lai izveidot jauno projektu

Sākumā vajag izveidot jauno VM:

```
conda create -n vm_nosaukums python=norādīt_versiju
```

Pēc tam to vajag aktivizēt:

```
conda activate virtuāla_mašīna
```

Instalēt nepieciešamas paķetes, piem., `django`:

```
conda install django
```

Pāriet uz projekta direktoriju. To var izdarīt vienkārši, dfailu pārlukā iekopē ceļu un ielīmē to konsolē:

```
cd ./ceļš_līdz_direktorijai
```

Izveido pašu projektu:

```
django-admin startproject projekta_nosaukums .
```

<mark style="background: #FFB86CA6;">Neaizmirsti par punktu!</mark>

Ja projekts veiksmīgi izveidojās, tad ievadi nākamo komandu, lai palaist projektu uz lokāla servera:

```
python manage.py runserver
```

Pēc tam taustiņu kombinācija `Crtl+C`, lai to apstādināt.

Pēc projekta izveidošanas, mēs pieslēgsim pašu `SQLite` pie projekta datu bāzes.
Atvēr `SQLite` un pievieno jauno datu bāzi, norādi ceļu līdz DB failam.
Pēc tam konsolē ievadi šādu komandu:

```
python manage.py migrate
```

Pašā `SQLite` nospied `disconnect` un `connect`. Jāparādas DB tabulām.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Anaconda Prompt (pamata komandas)]]
Nākama lapa >>> [[Skatu izveide]]

---