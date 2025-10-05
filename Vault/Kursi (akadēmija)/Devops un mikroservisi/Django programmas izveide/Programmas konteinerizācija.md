___

**Datums:** 2025-10-05
**Laiks:** 15:36
❚ **Tagi:** #devops 

---
# Programmas konteinerizācija

Šādi veidojam `image` failu:

```
docker build -t zenpanel_image .
```

Šādi mēs palaižam konteineri:

```
docker run -d --name zenPanel --network my-network -p 8000:8000 zenpanel_image
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Kursi (akadēmija)/Devops un mikroservisi/Django programmas izveide/Dockerfile izveide|Dockerfile izveide]]
Nākama lapa >>> [[Navigācija - Django programmas izveide]]

---