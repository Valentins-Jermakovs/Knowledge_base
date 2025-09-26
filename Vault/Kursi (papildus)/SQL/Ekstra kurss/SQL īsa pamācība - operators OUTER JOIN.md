___

**Datums:** 2025-08-04   
**Laiks:** 12:26 

❚ **Tagi:** #SQL 
⌬ **Priekšmets:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Ārējs savienojums

Tam pastāv trīs tipi:

- kreisais `LEFT`;
- labais `RIGHT`;
- pilnais `FULL` - tas ir arī pēc noklusējuma.
#### Arējs LEFT OUTER JOIN

Atgriež visu no kreisās tabulas, kas savienota ar labo.

```sql
SELECT Timepair.id 'timepair.id', start_pair, end_pair,
    Schedule.id 'schedule.id', date, class, number_pair, teacher, subject, classroom
FROM Timepair
    LEFT JOIN Schedule ON Schedule.number_pair = Timepair.id;
```
#### Arējs RIGHT OUTER JOIN

Atgriež visu no labās tabulas, kas savienota ar kreiso.
#### Ārējs FULL OUTER JOIN

Izvada visu, apvieno gan labo, gan kreiso tabulu.

```sql
SELECT *
FROM левая_таблица
LEFT JOIN правая_таблица
   ON правая_таблица.ключ = левая_таблица.ключ

UNION ALL

SELECT *
FROM левая_таблица
RIGHT JOIN правая_таблица
ON правая_таблица.ключ = левая_таблица.ключ
 WHERE левая_таблица.ключ IS NULL
```
#### Pamata vaicājumi dažādām tabulu apvienošanas iespējām

![[Pasted image 20250630094428.png]]
![[Pasted image 20250630094447.png]]
![[Pasted image 20250630094505.png]]
#### Praktiskais piemērs

```sql
SELECT Teacher.first_name,
	Teacher.last_name,
	COUNT(Schedule.id) AS amount_classes
FROM Teacher
	LEFT JOIN Schedule ON Schedule.teacher = Teacher.id
GROUP BY Teacher.first_name,
	Teacher.last_name
```

Šeit tiek izvadīts vārds, uzvārds un stundu skaits katram skolotājam.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[SQL īsa pamācība - operators INNER JOIN]]
Nākama lapa >>> [[SQL īsa pamācība - Agregātas funkcijas]]

___