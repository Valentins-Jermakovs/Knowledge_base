⏲ **Datums:** 2025-05-09   
⏲ **Laiks:** 10:39 
❚ **Tagi:**  #NoSQL 

⌬ **Objekts:**  `NoSQL`

---
### ⬢ Detalizēts apraksts
#### Pieslēgšanas procedūras

Sākuma vajag iegūt tokenu un url-vaicājumu no paša Swager UI.
Tokenu uzģenerēt, labāk ar Administratora tiesībām.
Lai iegūt url-vaicājumu, veic pašā Swager UI pieprasījumu uz kādu dokumentu kolekcijā, piem., ar filtru vai vienkārši, lai parāda visu kolekcijas saturu. Izvadā būs bloks ar URL saiti, iekopē to līdz `?` jautājuma zīmei, ja vajag izvilkt kolekcijas saturu. Ja vajag veikt konkrētu vaicājumu ar filtrāciju, kopē visu.

Pārej uz Reqbin vietni: [Online API Testing Tool \| Test Your API Online](https://reqbin.com/)
Tur pirmajā laukā ievadi savu iekopēto URL.
Pēc tam pārej uz sadaļu `Header` un kā `key` ievadi `X-Cassandra-Token` un pretī tam paša tokena vērtību. Nospied `Send`. Rezultātā jāparādās veiksmīgam pieprasījumam. 

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Dokumentu orientēta datu bāze]]
Nākama lapa >>> [[Navigācija - NoSQL DB]]

---