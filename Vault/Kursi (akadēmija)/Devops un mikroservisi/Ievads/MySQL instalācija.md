___

**Datums:** 2025-09-25
**Laiks:** 19:33
❚ **Tagi:** #devops 

---
# MySQL instalācija

<mark style="background: #ABF7F7A6;">Pirms darīt, izlasi!</mark>

Komandu jāizpilda `powershell` ar admina tiesībām!!!

Lai izveidot konteineri ar `MySQL`, izpildi šādu komandu:

```
docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql:tag
```

Šajā komandā pievērs uzmanību šādām vietām:

- `some-mysql` - šeit raksti nosaukumu savam konteinerim;
- `my-secret-pw` - šeit raksti savu paroli priekš `root` lietotāja;
- `tag` - versija, raksti `latest`.

Links uz oficiālo dokumentāciju >>> [hub.docker.com/\_/mysql](https://hub.docker.com/_/mysql)

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Portainer io instalācija]]
Nākama lapa >>> [[phpMyAdmin instalācija un savienošana ar MySQL]]

---