___
**Datums:** 2025-06-30   
**Laiks:** 14:30 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Kas ir CTE?
**CTE** jeb **kopīgais tabulas izteikums** ir pagaidu tabula, kuru var izmantot vaicājumā, lai padarītu to saprotamāku un strukturētāku.

**CTE tiek izveidots ar `WITH` operatoru** un darbojas tikai vaicājuma izpildes laikā - tā nav pastāvīga tabula datubāzē.

```sql
WITH Aeroflot_trips AS (
  SELECT plane, town_from, town_to 
  FROM Company 
  INNER JOIN Trip ON Trip.company = Company.id 
  WHERE name = "Aeroflot"
)
SELECT * FROM Aeroflot_trips;
```

Šeit mēs izveidojam **pagaidu tabulu `Aeroflot_trips`**, kas satur tikai "Aeroflot" lidojumus. Tad šo tabulu izmantojam galvenajā vaicājumā.
#### WITH operatora sintakse
```sql
WITH название_cte [(столбец_1 [, столбец_2 ] …)] AS (подзапрос)
    [, название_cte [(столбец_1 [, столбец_2 ] …)] AS (подзапрос)] …
```

Lietošanas kārtība:
- ievadīt operatoru `WITH`
- norādīt nosaukumu
- ievadīt `AS` un apakšvaicājumu
- atkārtot iepriekšējus soļus, līdz netiks izveidots pietiekams laicīgu tabulu skaits

```sql
WITH Aeroflot_trips (aeroflot_plane, town_from, town_to) AS
    (SELECT plane, town_from, town_to FROM Company
        INNER JOIN Trip ON Trip.company = Company.id WHERE name = "Aeroflot")

SELECT * FROM Aeroflot_trips;
```

![[Pasted image 20250630145317.png]]
#### Rekursīvs CTE
CTE var būt arī **rekursīvs** – tas ir noderīgi, piemēram, **darbinieku hierarhiju** analīzē.

```sql
WITH RECURSIVE Subordinates AS (
  SELECT id, name, managerId
  FROM Employees
  WHERE managerId = 1

  UNION ALL

  SELECT e.id, e.name, e.managerId
  FROM Employees e
  INNER JOIN Subordinates s ON e.managerId = s.id
)
SELECT * FROM Subordinates;
```

Šis vaicājums atrod **visus padotos**, kas pakļaujas konkrētam vadītājam (`managerId = 1`), arī padoto padotos, līdz pēdējam līmenim.

**Rekursīvās CTE izpildes darbības**
- **Sākotnējais datu kopums:** atlasa visus darbiniekus ar managerId=1 (John Smith tiešie padotie).
- **Rekursīvā daļa:** katram darbiniekam, kas atlasīts sākotnējā datu kopā, atlasa viņa padotos (kur managerId ir atlasītā darbinieka ID).
- **Apvienošana:** sākotnējā datu kopuma un rekursīvās daļas rezultāti tiek apvienoti, izmantojot `UNION ALL`.
- **Rekursija:** process tiek atkārtots katram jaunam ziņojumu kopumam, līdz ir atlasīti visi hierarhijas līmeņi.

---
### ⇄ Saistības
Avots >>> [Обобщенное табличное выражение, WITH — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/operator-with)
Iepriekšēja lapa >>> [[Korelēti apakšvaicājumi]]
Nākama lapa >>> [[Vaicājumu apvienošana]]
___