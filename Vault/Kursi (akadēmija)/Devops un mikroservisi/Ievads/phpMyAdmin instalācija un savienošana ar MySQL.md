___

**Datums:** 2025-09-25
**Laiks:** 19:43
❚ **Tagi:** #devops 

---
# phpMyAdmin instalācija un savienošana ar MySQL

<mark style="background: #ABF7F7A6;">Pirms darīt, izlasi!</mark>

Lai viss darbotos, ielādē `phpMyAdmin` `Image` failu un iestati `MySQL` konteineri!
Lai saslēgt `phpMyAdmin` kopā ar `MySQL` konteineri, izmanto šo komandu:

```
docker run --name phpmyadmin -d --link mysql_db_server:db -p 8080:80 phpmyadmin
```

Pievērs uzmanību šādam lietām:

- `mysql_db_server` - šeit raksti sava iepriekš veidota `MySQL` konteinera nosaukumu.

Links uz oficiālo dokumentāciju >>> [Docker Hub](https://hub.docker.com/_/phpmyadmin)

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[MySQL instalācija]]
Nākama lapa >>> [[šablons]]

---