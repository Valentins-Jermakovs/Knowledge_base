___

**Datums:** 2025-09-27
**Laiks:** 15:08
❚ **Tagi:** #devops 

---
# Tīkla izveide

Pirms veidot savā starpa saistītos konteinerus, ieteicams izveidot `Docker` tīklu. Tas ir tāds iekšējais tīkls, ko izmanto konteineri, lai savā starpā sazināties. Tā kā konteineri tiks izvietoti kopējā tīklā, tie savā starpā var versites pēc konteineru (serveru) nosaukumiem.

| Komanda                         | Skaidrojums                                 |
| ------------------------------- | ------------------------------------------- |
| docker network ls               | Apskatīt dockera tīklus                     |
| docker rm <tīkla nosaukums>     | Izdzēst norādīto tīklu                      |
| docker create <tīkla nosaukums> | Izveidot docker tīklu ar norādīto nosaukumu |


---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - Docker pamati]]
Nākama lapa >>> [[MySQL konteinera izveide]]

---