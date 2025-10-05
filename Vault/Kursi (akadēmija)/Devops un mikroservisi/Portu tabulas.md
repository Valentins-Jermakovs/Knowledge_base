___

**Datums:** 2025-10-05
**Laiks:** 15:45
❚ **Tagi:** #devops 

---
# Portu tabulas

Biežāk izmantotie porti konteineros (pēc servisa veida)

| Serviss / Lietojums            | Konteinera tips                 | Iekšējais ports (konteinerā) | Piezīme                               |
| ------------------------------ | ------------------------------- | ---------------------------- | ------------------------------------- |
| Django / Flask / FastAPI       | Tīmekļa aizmugure (Python)      | `8000`                       | Noklusētais Django/uvicorn ports      |
| Node.js / Express              | Tīmekļa aizmugure (JavaScript)  | `3000`                       | Dažreiz `8080`                        |
| React / Vue izstrādes serveris | Frontend                        | `5173`, `8080`, `3000`       | Atkarīgs no ietvara                   |
| PostgreSQL                     | Datu bāze                       | `5432`                       | Standarta PostgreSQL ports            |
| MySQL / MariaDB                | Datu bāze                       | `3306`                       | Standarts                             |
| Redis                          | Kešatmiņa                       | `6379`                       | Bieži lietots kopā ar Django vai Node |
| MongoDB                        | Datu bāze                       | `27017`                      | Standarts                             |
| Nginx                          | Reverse proxy / statiskie faili | `80`, `443`                  | HTTP un HTTPS                         |
| phpMyAdmin                     | Administrēšanas rīks            | `8080` vai `8081`            | Web saskarne datu bāzēm               |
| Prometheus                     | Monitorings                     | `9090`                       | Metriku serveris                      |
| Grafana                        | Monitoringa saskarne            | `3000`                       | Web saskarne Grafanai                 |

Saimniekdatora (host) porti un to izmantošanas ieteikumi

| Portu diapazons | Statuss                            | Ieteikumi                                                                  |
| --------------- | ---------------------------------- | -------------------------------------------------------------------------- |
| `0–1023`        | **Sistēmas porti**                 | Nelietot — tos izmanto sistēmas servisi (piem., 22 SSH, 80/443 HTTP/HTTPS) |
| `1024–49151`    | **Reģistrētie porti (IANA)**       | Var lietot, bet jāpārbauda, vai nav konflikta ar esošiem servisiem         |
| `49152–65535`   | **Dinamiskie (ephemerālie) porti** | Droši izmantojami lokālai izstrādei vai pagaidu konteineriem               |

Drošu host portu piemēri (ieteikta shēma)

| Lietojums             | Konteinera ports | Host ports (ieteiktais) | Piezīme                           |
| --------------------- | ---------------- | ----------------------- | --------------------------------- |
| Django API            | `8000`           | `8000` vai `8080`       | Noklusētais servera ports         |
| Node.js API           | `3000`           | `3001`                  | Ja `3000` jau aizņemts frontendam |
| PostgreSQL            | `5432`           | `5433`                  | Ja uz hosta jau ir PostgreSQL     |
| Redis                 | `6379`           | `6380`                  | Alternatīvs ports, ja konflikts   |
| Frontend (Vue/React)  | `5173`           | `5173` vai `5174`       | Izstrādes serveris                |
| Grafana               | `3000`           | `4000`                  | Lai nesajauktu ar Node.js         |
| Nginx (reverse proxy) | `80 / 443`       | `80 / 443`              | Parasti tieši piesaistīts hostam  |

```
docker run -d -p 8081:8000 mans_app
```

- `8081` - mana hosta ports
- `8000` - konteinera ports

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - Devops un mikroservisi]]

---