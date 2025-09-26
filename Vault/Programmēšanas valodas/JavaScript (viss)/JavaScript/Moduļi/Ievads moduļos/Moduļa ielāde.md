___

**Datums:** 2025-08-30
**Laiks:** 12:40
❚ **Tagi:** #javascript 

---
### Moduļa ielāde

Lai ielādēt moduļus, izveidosim failu `index.html` un ievietosim tajā šādu kodu:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>METANIT.COM</title>
</head>
<body>
<script type="module" src="main.js"></script>
</body>
</html>
```

Atribūts `type="module"` ļauj ielādēt `main.js` moduli, kas satur citus moduļus.

Atsevišķi veidojam server failu `server.js`, kas tiks palaists izmantojot `node.js`:

```js
const http = require("http");
const fs = require("fs");
   
http.createServer(function(request, response){
       
    // получаем путь после слеша
    let filePath = request.url.substring(1);
    if(filePath == "") filePath = "index.html"; 
    fs.readFile(filePath, function(error, data){
               
        if(error){
            response.statusCode = 404;
            response.end("Resourse not found!");
        }   
        else{
            if(filePath.endsWith(".js")) response.setHeader("Content-Type", "text/javascript");
            response.end(data);
        }
    });
}).listen(3000, function(){
    console.log("Server started at 3000");
});
```

Servera izveidei tiek izmantota funkcija `http.createServer()`.
Failu lasīšanai un nosūtīšanai tiek izmantota funkcija `fs.readFile()`.

Ir vērts atzīmēt, ka, nosūtot `js` moduļus, mums jāiestata nosūtāmā satura mime-tips uz "text/javascript":

```js
if(filePath.endsWith(".js")) response.setHeader("Content-Type", "text/javascript");
```

Beigās palaižam serveri no kataloga, kur atrodas pats projekts:

>node server.js

Rezultātā tiks palaista lapa, kas izpildīs moduļa funkcijas:

![[Pasted image 20250830125506.png]]

---
### ⇄ Saistības

Avots >>> [JavaScript \| Введение в модули](https://metanit.com/web/javascript/19.1.php)
Iepriekšēja lapa >>> [[Moduļa pieslēgšana (imports)]]
Nākama lapa >>> [[Navigācija - Ievads moduļos]]

---