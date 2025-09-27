___

**Datums:** 2025-09-27
**Laiks:** 15:19
❚ **Tagi:** #devops 

---
# phpMyAdmin konteinera izveide

Izmanto šo komandu, lai izveidot `docker` konteineri, kas satur `phpMyAdmin` vadības paneli:

```
docker run -d --name pma --network my-network -e PMA_ARBITRARY=1 -p 8080:80 phpmyadmin
```

Šeit ir dažas jaunas opcijas, salīdzinājumā ar iepriekšējo rakstu:

- `PMA_ARBITARY=1` šis norāda, kā tu varēsi izmantot šo vadības paneli ar vairākiem serveriem, jo parasti `phpMyAdmin` pieslēdz pie viena konkrēta servera. Tā kā šeit vadības panelis tiek pieslēgts pie viena kopēja konteineru tīkla, logā `Server` būs pietiekami ievadīt servera nosaukumu.
- `phpmyadmin` norāda izmantot docker image (dockera repozitoriju).

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[MySQL konteinera izveide]]
Nākama lapa >>> [[Navigācija - Docker pamati]]

---