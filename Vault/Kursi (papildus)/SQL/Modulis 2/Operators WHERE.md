___
**Datums:** 2025-06-27   
**Laiks:** 15:57 
❚ **Tagi:** #SQL
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### WHERE sintakse

```SQL
SELECT [DISTINCT] поля_таблиц FROM наименование_таблицы
WHERE условие_на_ограничение_строк
[логический_оператор другое_условие_на_ограничение_строк];
```

Piemērs ar `WHERE` izmantošanu:

```SQL
SELECT * FROM Student
WHERE first_name = "Grigorij" AND YEAR(birthday) > 2000;
```

Šajā piemērā tiek izmantoti:
- 2 salīdzinājuma operatori `first_name="Grigorij"` un `YEAR(bityhday)>20;`
- viens loģiskais operators `AND`

>Atceries! `WHERE` tiek rakstīts pašās beigās!
#### Salīdzinājuma operatori
Salīdzināšanas operatori tiek izmantoti, lai salīdzināt 2 vērtības, rezultāts būs vien no:
- `true`
- `false`
- `NULL`

| Operators           | Apzīmējums    | Apraksts                                                                                              |
| ------------------- | ------------- | ----------------------------------------------------------------------------------------------------- |
| Vienādība           | `=`           | Ja vienāds, tad `1`. Ja nav vienāds, tad `0`.                                                         |
| Ekvivalence         | `<=>`         | Tas pats, kas vienādība, bet ar vienu atšķirību. `NULL` un `NULL` kopā dos `1`. Pretējā gadījumā `0`. |
| Nevienadība         | `<>` vai `!=` | Ja abas vērtības nav vienādas, tad būs `1`. Pretējā gadījumā `0`.                                     |
| Mazāks              | `<`           | Ja mazāks par, tad `1`. Pretējā gadījumā `0`.                                                         |
| Mazāks, vienāds     | `<=`          | Ja mazāks, vienāds, tad `1`. Pretējā gadījumā `0`.                                                    |
| Lielāks             | `>`           | Ja lielāks, tad `1`. Pretējā gadījumā `0`.                                                            |
| Lielāks vai vienāds | `>=`          | Ja lielāks vai vienāds, tad `1`. Pretējā gadījumā `0`.                                                |
#### Loģiskie operatori
Loģiskie operatori nepieciešami, lai savienot salīdzināšanas operatorus.

| Operators | Apraksts                                                  |
| --------- | --------------------------------------------------------- |
| `NOT`     | Maina salīdzināšanas operatora vērtību uz pretējo         |
| `OR`      | Atgriezīs `TRUE`, ja viens no salīdzinājumiem būs patiess |
| `AND`     | Atgriezīs `TRUE`, ja abi salīdzinājumi ir patiesi.        |
| `XOR`     | Atgriezīs `TRUE`, tikai, ja ir patiess 1 salīdzinājums.   |
Piemērs, izvadīt lidojumus, kur lidmašīnas modelis ir `Boeing` un izlidoja ne no `London`:

```SQL
SELECT * FROM Trip
WHERE plane = 'Boeing' AND NOT town_from = 'London';
```


---
### ⇄ Saistības
Avots >>> [Условный оператор WHERE — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/conditional-where-operator)
Iepriekšēja lapa >>> [[Atkārtojumu izslēgšana, DISTINCT]]
Nākama lapa >>> [[Operatori IS NULL, BETWEEN, IN]]
___