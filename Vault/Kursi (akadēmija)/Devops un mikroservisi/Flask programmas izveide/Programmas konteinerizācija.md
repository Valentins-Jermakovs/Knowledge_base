___

**Datums:** 2025-09-27
**Laiks:** 15:54
❚ **Tagi:** #devops 

---
# Programmas konteinerizācija

Lai veidot un pārvaldīt docker pašveidoto konteineri, var izmantot šādas te komandas:

```
docker build -t flask_app_image .
```

Šeit punkts esot obligāts.

- `docker build` - liekam dockerim veidot konteineri;
- `-t <image_name>` - šeit veidojam `image` failu, no kura tiks veidots konteiners;
- `.` punkts (obligāts), norāda tagadējo mapi.

```
docker run -d --name flask_app_container --network my-network -p 5000:5000 flask_app_image
```

Šeit jau zināms.

```
docker stop flask_app_container
```

Šī komanda apstādina norādīta konteinera darbību.

```
docker rm flask_app_container
```

Šī komanda izdzēš norādīto konteineri.

**Autora papildinājums, svarīgi!**

Lai iegūt pilnu `dependency` sarakstu, ja tiek izmantota `anaconda`, izmanto šādu komandu:

```
pip list --format=freeze
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Kursi (akadēmija)/Devops un mikroservisi/Flask programmas izveide/Dockerfile izveide]]
Nākama lapa >>> [[Navigācija - Flask]]

---