⏲ **Datums:** 2025-05-10   
⏲ **Laiks:** 11:35 
❚ **Tagi:**  #NoSQL 

⌬ **Objekts:**  `NoSQL`

---
### ⬢ Detalizēts apraksts
#### Sākums
Lai pieslēgt API šādai DB, izmantojot `reqbin` [Online API Testing Tool \| Test Your API Online](https://reqbin.com/)
Nepieciešams iegūt `Graphql` URL un `tokenu`.

![[Pasted image 20250510113656.png]]
URLs, kas tiks izmantots.
#### Reqbin iestatīšana
Lai iegūt datus šajā sistēma, sākumā ielīmē URL adresi laukā un nomaini uz `POST`.
![[Pasted image 20250510113813.png]]

Pēc tam pārej uz sadaļu `Headers`, pie `key` ievadi `X-Cassandra-Token`, pretī tam `tokena` vērtību.
![[Pasted image 20250510113927.png]]
#### Pieprasījuma veikšana
Pārej uz `Body` -> `JSON`
Ja mēs gribam iegūt visu tabulas saturu:
![[Pasted image 20250510114200.png]]
Ja mums vajag meklēt pēc `Partition key`:
![[Pasted image 20250510121112.png]]
Meklēšana gan pēc `Partition key`, gan pēc `indeksa atslēgas`:
![[Pasted image 20250510121155.png]]
Meklēšana tikai pēc `indeksa atslēgas`
![[Pasted image 20250510121407.png]]

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[key-value orientēta datu bāze]]
Nākama lapa >>> [[Navigācija - NoSQL DB]]

---