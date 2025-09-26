___
**Datums:** 2025-07-01   
**Laiks:** 17:37 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Logu rāmji

> [!NOTE] Logs
> Logs ir dinamisks rindu kopums, kas "slīd" cauri jūsu vaicājuma rezultātam, katrai rindai ģenerējot atšķirīgus datu kopumus atkarībā no jūsu norādītās loga definīcijas.

#### Logs vs Partīcija

Partīcija (`PARTITION BY`) ir visa rezultātu kopas sadalīšana nesadalītās apakškopās, kur katra apakškopa satur rindas ar vienādām vērtībām vienā vai vairākās kolonnās.

![[partitions_visualisation.webp]]

Logs: Norāda, kuras konkrētās rindas katrā nodalījumā tiks izmantotas, lai aprēķinātu loga funkciju katrai rindai.

![[windows_visualisation.webp]]

#### Loga robežu noteikšana

Izmantojot `ROWS` vai `RANGE` sintaksi, mēs varam noteikt, kurš datu logs tiks nodots loga funkcijai, lai aprēķinātu pašreizējās rindas vērtību.

```sql
SELECT <оконная_функция>(<поле_таблицы>)
OVER (
      ...
      ROWS|RANGE BETWEEN <начало границы окна> AND <конец границы окна>
)
```

Piemēram, ja mēs vēlamies, lai loga funkcija aprēķinā iekļautu tikai divus iepriekšējos ierakstus un pašreizējo rindu, sintakse izskatītos šādi:

```sql
... ROWS|RANGE BETWEEN 2 PRECEDING AND CURRENT ROW
```

Ja vēlamies, lai pašreizējā rinda un visas nākamās rindas tiktu nodotas loga funkcijai, sintakse izskatīsies šādi:

```sql
... ROWS|RANGE BETWEEN CURRENT ROW AND UNBOUNDED FOLLOWING
```

**Iespējamās logu apmaļu definīcijas:**

- `UNBOUNDED PRECEDING` - visas rindas pirms pašreizējās rindas
- `N PRECEDING` - N rindas pirms pašreizējās rindas
- `CURRENT ROW` - pašreizējā rinda
- `N FOLLOWING` - N rindas pēc pašreizējās rindas
- `UNBOUNDED FOLLOWING` - visas nākamās rindas

![[window-definition.webp]]

#### ROWS vs RANGE
`ROWS` definē loga robežas, pamatojoties uz rindu fizisko pozīciju, savukārt `RANGE` definē loga robežas, pamatojoties uz kolonnu vērtībām.

![[rows_example.webp]]

![[range_example.webp]]

---
### ⇄ Saistības
Avots >>> [Рамки окон в оконных функциях — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/windows-functions-frames)
Iepriekšēja lapa >>> [[Kārtošana logā]]
Nākama lapa >>> [[Logu pamatfunkcijas]]
___