___

**Datums:** 2025-09-27
**Laiks:** 15:14
❚ **Tagi:** #devops 

---
# MySQL konteinera izveide

Izmanto šo komandu, lai izveidot `docker` konteineri, kas satur `MySQL` datubāzi:

```
docker run --name mysql1 --network my-network -e MYSQL_ROOT_PASSWORD=root123 -p 3307:3306 -d mysql:latest
```

Šeit ir dažas opcijas:

- `--name` šeit tu norādi servera vārdu;
- `--network` šeit tu pieslēdz docker tīklu;
- `MYSQL_ROOT_PASSWORD` šeit tu norādi `root` lietotāja paroli;
- `-p 3307:3306` šeit tu norādi portu;
- `-d` norāda uz to, kā konteiners tiks veidots asinhroni, tas nozīmē kā pēc tā izveides varēsi turpināt strādāt konsolē;
- `mysql:latest` šeit norādi izmantot pēdējo `mysql` versiju, kas ir pieejama dockera repozitorijos.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Tīkla izveide]]
Nākama lapa >>> [[phpMyAdmin konteinera izveide]]

---