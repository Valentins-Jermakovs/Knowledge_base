___
**Datums:** 2025-07-02   
**Laiks:** 12:23 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Tabulas izveide

Pirms tabulas izveides ir jāizvēlas datubāze, kurā tabula tiks ierakstīta. To var izdarīt, izmantojot `USE` komandu:

```sql
USE имя_базы_данных;
```

Lai izveidotu tabulu, izmantojiet komandu` CREATE TABLE`. Tās pamata sintakse ir šāda:

```sql
CREATE TABLE [IF NOT EXIST] имя_таблицы (
     столбец_1 тип_данных,
    [столбец_2 тип_данных,]
    ...
    [столбец_n тип_данных,]
);
```

```sql
CREATE TABLE Users (
    id INT,
    name VARCHAR(255),
    age INT
);
```

#### Papildus kolonnu definīcijas opcijas

Papildus kolonnas nosaukumam un tipam var būt nepieciešams pievienot šādus papildu parametrus:

- `PRIMARY KEY` - Norāda kolonnu vai kolonnu kopu kā primāro atslēgu.
- `AUTO_INCREMENT` - Norāda, ka šīs kolonnas vērtība tiks automātiski palielināta, kad tabulai tiks pievienoti jauni ieraksti.
- `UNIQUE` - Norāda, ka visu ierakstu vērtībām šajā kolonnā jābūt atšķirīgām vienai no otras.
- `NOT NULL` - Norāda, ka šīs kolonnas vērtībām jābūt atšķirtām no `NULL`.
- `DEFAULT` - Norāda noklusējuma vērtību.

```sql
CREATE TABLE Users (
    id INT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    age INT NOT NULL DEFAULT 18
);
```

#### Tabulas apraksts

Lai skatītu izveidotās tabulas aprakstu, varat izmantot operatoru `DESCRIBE`.

```sql
DESCRIBE Users;
```

![[Pasted image 20250702123046.png]]

#### Papildus parametri tabulai

`Primary key` pievienošana tabulai:

```sql
CREATE TABLE Users (
    id INT,
    name VARCHAR(255) NOT NULL,
    age INT NOT NULL DEFAULT 18,
    PRIMARY KEY (id)
);
```

`Foreign key` pievienošana tabulai:

```sql
FOREIGN KEY (<столбец_1>, <столбец_n>)
REFERENCES <внешняя_таблица> (<столбец_во_внешней_таблице_1>, <столбец_во_внешней_таблице_n>)
[ON DELETE действие]
[ON UPDATE действие]
```

```sql
CREATE TABLE Users (
    id INT,
    name VARCHAR(255) NOT NULL,
    age INT NOT NULL DEFAULT 18,
    company INT,
    PRIMARY KEY (id),
    FOREIGN KEY (company) REFERENCES Companies (id)
);
```

Izmantojot ārējās atslēgas, varat definēt pašreizējā ieraksta darbību, kad ieraksts, uz kuru tas atsaucas, tiek modificēts vai dzēsts.

```sql
CREATE TABLE Users (
    id INT,
    name VARCHAR(255) NOT NULL,
    age INT NOT NULL DEFAULT 18,
    company INT,
    PRIMARY KEY (id),
    FOREIGN KEY (company) REFERENCES Companies (id)
    ON DELETE RESTRICT ON UPDATE CASCADE
);
```

`ON DELETE RESTRICT` nozīmē, ka, mēģinot dzēst kompāniju, kurai ir dati tabulā `Users`, datubāze to neļaus izdarīt:

```sql
Cannot delete or update a parent row: a foreign key constraint fails
```

#### Tabulas dzēšana

Lai izdzēst tabulu, izmanto operatoru `DROP TABLE`.

```sql
DROP TABLE [IF EXIST] имя_таблицы;
```

---
### ⇄ Saistības
Avots >>> [Создание и удаление таблиц — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/create-table)
Iepriekšēja lapa >>> [[Datu bāžu izveide un dzēšana]]
Nākama lapa >>> [[Datu tipi tabulu kolonnām]]
___