___

**Datums:** 2025-09-12
**Laiks:** 10:43
❚ **Tagi:** #back-end #python 

---
### Anaconda Prompt

#### Anaconda Prompt komandas

| Komada                                              | Skaidrojums                                                             |
| --------------------------------------------------- | ----------------------------------------------------------------------- |
| conda create -n vm_nosaukums python=norādīt_versiju | izveidot jauno virtuālo mašīnu                                          |
| conda activate virtuāla_mašīna                      | pārslēgties uz norādīto virtuālo mašīnu                                 |
| conda info --envs                                   | apskatīt pieejamas VM                                                   |
| conda install paķetes_nosaukums                     | instalēt norādīto paķeti                                                |
| conda list                                          | apskatīt sainstalētas conda paķetes                                     |
| django-admin startproject projekta_nosaukums .      | Palaist projektu no esošas direktorijas. *Obligāti punktu beigās likt!* |
| python manage.py runserver                          | palaist projektu uz lokāla servera                                      |

#### Pip menedžera komandas
| Komanda                       | Skaidrojums                         |
| ----------------------------- | ----------------------------------- |
| pip install paķetes_nosaukums | instalēt paķetes caur pip menedžeri |
| pip list                      | apskatīt saisntalētas pip paķetes   |
#### `SQLite` pieslēgšana pie projekta

Lai iedarbināt datu bāze `SQLite`:

Uzlikt uz datora pašu `SQLite`, pievienot DB mapi, norādīt ceļu līdz projekta DB failam.

Pēc tam `anaconda prompt`:

```
python manage.py migrate
```

*Piezīme. Lokālam serverim jābūt izslēgtam `Ctrl+C`.*


---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - back-end python]]
Nākama lapa >>> [[Jaunā projekta izveide]]

---