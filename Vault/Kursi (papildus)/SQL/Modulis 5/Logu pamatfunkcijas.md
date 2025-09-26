___
**Datums:** 2025-07-01   
**Laiks:** 17:59 
❚ **Tagi:** #SQL
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Logu pamatfunkcijas

![[categories_of_windows_functions.webp]]

#### Agregāt-funkcijas

Funkcijas:
- `SUM` - summē
- `COUNT` - saskaita ierakstu daudzumu
- `AVG` - aprēķina vidējo
- `MAX` - atrod maksimālo vērtību
- `MIN` - atrod minimālo vērtību

```sql
SELECT id,
	home_type,
	price,
	SUM(price) OVER(PARTITION BY home_type) AS 'Sum',
	COUNT(price) OVER(PARTITION BY home_type) AS 'Count',
	AVG(price) OVER(PARTITION BY home_type) AS 'Avg',
	MAX(price) OVER(PARTITION BY home_type) AS 'Max',
	MIN(price) OVER(PARTITION BY home_type) AS 'Min'
FROM Rooms;
```

#### Ranžējošās funkcijas

`ROW_NUMBER` - atgriež rindas numuru, tiek izmantots numerācijai
`RANK` - piešķir rangu ierakstam, sākas no 1
`DENSE_RANK` - piešķir rangu, bet atšķirība no `RANK`, neizlaiž nākamo, ja atgriež kopējām.

```sql
SELECT id,
	home_type,
	price,
	ROW_NUMBER() OVER(PARTITION BY home_type ORDER BY price) AS 'row_number',
	RANK() OVER(PARTITION BY home_type ORDER BY price) AS 'rank',
	DENSE_RANK() OVER(PARTITION BY home_type ORDER BY price) AS 'dense_rank'
FROM Rooms;
```

#### Logu nobīdes funkcijas

`LAG` - atgriež datus no iepriekšējām rindām
`LEAD` - vēršas pie nākamo rindu datiem
`FIRST_VALUE` - atgriež pirmo vērtību logā
`LAST_VALUE` - atgriež pēdējo vērtību logā

```sql
SELECT id,
	home_type,
	price,
	LAG(price) OVER(PARTITION BY home_type ORDER BY price) AS 'lag',
	LAG(price, 2) OVER(PARTITION BY home_type ORDER BY price) AS 'lag_2',
	LEAD(price) OVER(PARTITION BY home_type ORDER BY price) AS 'lead',
	FIRST_VALUE(price) OVER(PARTITION BY home_type ORDER BY price) AS 'first_value',
	LAST_VALUE(price) OVER(PARTITION BY home_type ORDER BY price) AS 'last_value'
FROM Rooms;
```

---
### ⇄ Saistības
Avots >>> [Типы оконных функций — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/types-of-windows-functions)
Iepriekšēja lapa >>> [[Logu rāmji]]
Nākama lapa >>> [[Transakcijas]]
___