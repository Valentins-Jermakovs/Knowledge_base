___
**Datums:** 2025-06-27   
**Laiks:** 15:07 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Iebūvētas funkcijas
SQL ir iebūvētas funkcijas, ko mēs varam izmantot, piemēram `UPPER`, kas izvadīs teksta rindu `Capsā`

```SQL
SELECT UPPER("Hello world") AS upper_string;
```

Funkcijas var kā saņemt argumentu, tā arī strādāt bez tā.
#### Funkciju piemēri
- `LOWER` atgriež teksta rindu zemā reģistrā
- `YEAR` atgriež gadu norādītajam datumam
- `INSTR` meklē teksta apakšrindu un atgriež tās pirmā simbola pozīciju
- `LENGTH` atgriež norādītas teksta rindas garumu

```SQL
SELECT LOWER('SQL Academy') AS lower_string;
```
Atgriezīs `sql academy`

```SQL
SELECT YEAR("2022-06-16") AS year;
```
Atgriezīs `2022`

```SQL
SELECT INSTR('sql-academy', 'academy') AS idx;
```
Atgriezīs `5`

```SQL
SELECT LENGTH('sql-academy') AS str_length;
```
Atgriezīs `11`

#### Sarežģītāka vaicājuma piemērs
Šajā piemēra tiek izvadīts ģimenes locekļa pilnais vārds un tā uzvārda garums:
```SQL
SELECT member_name,
	LENGTH(member_name) - INSTR(member_name, ' ') AS lastname_length
FROM FamilyMembers;
```

---
### ⇄ Saistības
Avots >>> [Применение функций — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/using-functions)
Iepriekšēja lapa >>> [[Literāļi SQL]]
Nākama lapa >>> [[Atkārtojumu izslēgšana, DISTINCT]]
___