___
**Datums:** 2025-07-01   
**Laiks:** 17:03 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Pārtīcijas logu funkcijās

> [!NOTE] Partīcijas
> Tas ir rindu apakškopas, kas piešķirtas loga funkcijai, pamatojoties uz vienu vai vairākām tabulas kolonnām.

![[3 1.webp]]

```sql
SELECT <оконная_функция>(<поле_таблицы>)
OVER (
    PARTITION BY <столбцы_для_разделения>
)
```

```sql
SELECT
    home_type, price,
    AVG(price) OVER (PARTITION BY home_type) AS avg_price
FROM Rooms
```

Tāpat to var veikt pa vairākām kolonnām:

```sql
SELECT
    home_type, has_tv, price,
    AVG(price) OVER (PARTITION BY home_type, has_tv) AS avg_price
    FROM Rooms
```

Šeit parametrs `PARTITION BY` `home_type` un `has_tv` izveido unikālas sadaļas katrai `home_type` un `has_tv` kombinācijai, ļaujot aprēķināt vidējo mājas cenu pašreizējai mājas kategorijai ar vai bez televizora.

![[2-columns-partition.webp]]

---
### ⇄ Saistības
Avots >>> [Партиции в оконных функциях — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/partitions)
Iepriekšēja lapa >>> [[Loga funkcijas]]
Nākama lapa >>> [[Kārtošana logā]]
___