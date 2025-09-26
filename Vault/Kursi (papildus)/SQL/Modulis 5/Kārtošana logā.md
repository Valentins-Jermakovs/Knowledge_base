___
**Datums:** 2025-07-01   
**Laiks:** 17:25 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Kārtošana logā
Kārtošana SQL loga funkcijās ir atslēga uz uzlabotu datu analīzi. Tā ļauj organizēt datus noteiktā grupā vai logā, nodrošinot precīzākus un mērķtiecīgākus apkopotos aprēķinus. Tas ir īpaši noderīgi, strādājot ar laika rindām, kur notikumu secība ir svarīga, vai ranžējot datus grupās.

#### Piemērs: Rezervācijas dati

**Sākotnējs vaicājums bez kārtošanas:**

```sql
SELECT user_id,
       start_date,
       total AS reservation_price,
       SUM(total) OVER (
           PARTITION BY user_id
       ) AS total_expenses
FROM Reservations;
```

Rezultāts: katram lietotājam parādās **kopējā summa**, bet **bez laika secības**.

**Uzlabots vaicājums (ar kārtošanu):**

```sql
SELECT user_id,
       start_date,
       total AS reservation_price,
       SUM(total) OVER (
           PARTITION BY user_id
           ORDER BY start_date
       ) AS cumulative_total
FROM Reservations;
```

Rezultāts: katram lietotājam redzams, **kā tēriņi uzkrājās hronoloģiski**.

Kā tas darbojas?
- `PARTITION BY user_id` – sadala datus pa lietotājiem.
- `ORDER BY start_date` – sakārto katra lietotāja rezervācijas pēc datuma.
- Tiek piemērots **noklusētais logs**: `RANGE BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW`.

Tas nozīmē: **no pirmās rindas līdz pašreizējai**, veidojot **uzkrājošu summu** katram lietotājam.

**Pilnais sintakses modelis:**

```sql
SELECT funkcija(kolonna)
OVER (
  [PARTITION BY ...]
  [ORDER BY ...]
  [ROWS|RANGE ...]
)
```

- `PARTITION BY` – sadala logus.
- `ORDER BY` – nosaka aprēķinu secību.
- `ROWS` / `RANGE` – nosaka loga **robežas** (piem., 1 rinda iepriekš + šī rinda utt.). Ja nav norādīts, tiek pieņemts uzkrājošs logs pēc kārtas.

---
### ⇄ Saistības
Avots >>> [Сортировка внутри окна — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/sorting-in-windows-functions)
Iepriekšēja lapa >>> [[Pārtīcijas logu funkcijās]]
Nākama lapa >>> [[Logu rāmji]]
___