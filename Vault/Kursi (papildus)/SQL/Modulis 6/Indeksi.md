___
**Datums:** 2025-07-02   
**Laiks:** 13:34 
❚ **Tagi:** #SQL
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Indeksi

Indeksi darbojas līdzīgi kā indeksi grāmatā, ļaujot ātri atrast informāciju, neizlasot visu tekstu. Tās ir īpašas tabulas, kuru rindas, atšķirībā no parastajām datu tabulām, ir sakārtotas stingri noteiktā secībā. Taču indekss satur nevis visus datus par ierakstu, bet tikai kolonnu (vai kolonnas), kas izmantotas rindu atrašanai datu tabulā, kā arī informāciju, kas apraksta, kur šī rinda fiziski atrodas. Tātad indeksu uzdevums ir atvieglot tabulas rindu un kolonnu apakškopas atrašanu, nepārskatot katru tabulas rindu.

#### Indeksa izveide

```sql
CREATE INDEX indeksa_nosaukums
    ON tabulas_nosaukums (kolonna);
```

```sql
CREATE INDEX idx_email
    ON Users (email);
```

#### Indeksa dzēšana

```sql
DROP INDEX indeksa_nosaukums ON tabulas_nosaukums;
```

```sql
DROP INDEX idx_email ON Users;
```

#### Unikāla indeksa izveide

```sql
CREATE UNIQUE INDEX indeksa_nosaukums
    ON tabulas_nosaukums (kolonna);
```

```sql
CREATE UNIQUE INDEX idx_email
    ON Users (email);
```

Šeit, ja tu mēģināsi indeksa laukā ierakstīt vērtību, kas jau figurēja iepriekš, DB pārvaldības sistēma izdos kļūdu, jo katram tādam indeksam jābūt unikālam.

#### Vairāku kolonnu indeksi

Šajā piemēra tiek veidots viens kopīgais indekss uz vairākām (2) kolonnām.

```sql
CREATE INDEX indeksas_nosaukums
    ON tabulas_nosaukums (kolonna_1, kolonna_2);
```

```sql
CREATE INDEX idx_full_name
    ON Student (last_name, first_name);
```

#### Indeksu izmantošana

DB pārvaldības sistēma automātiski veiks meklēšanu pa tabulai, izmantojot indeksus, ja tie figurēs vaicājumā. Piemēram, šeit, sistēma var meklēt izmantojot kopējo indeksu `idx_full_name` vai atsevišķus indeksus.

```sql
SELECT id, first_name, last_name
  FROM Student
  WHERE first_name LIKE 'A%' AND last_name LIKE 'L%'
```

---
### ⇄ Saistības
Avots >>> [Индексы в SQL — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/indexes)
Iepriekšēja lapa >>> [[VIEW]]
Nākama lapa >>> [[SQL ierobežojumi]]
___