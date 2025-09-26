___
**Datums:** 2025-07-01   
**Laiks:** 18:44 
❚ **Tagi:** #SQL
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Transakciju izveide
Transakcija ir SQL komandu secība, kas tiek izpildīta kā **viens vienots loģisks bloks**. Tā nodrošina datu drošību: vai nu izmaiņas tiek pielietotas pilnībā (**COMMIT**), vai netiek veiktas vispār (**ROLLBACK**).

```sql
START TRANSACTION;

-- Iegūstam sūtītāja konta bilanci
SELECT @balance := user_balance FROM accounts WHERE user_id = 1;

-- Ja bilance nepietiekama – atceļam
IF @balance < 1000 THEN
  ROLLBACK;
END IF;

-- Ja saņēmēja konts neeksistē – atceļam
SELECT @exists := COUNT(*) FROM accounts WHERE user_id = 2;
IF @exists = 0 THEN
  ROLLBACK;
END IF;

-- Atjaunojam abu lietotāju kontus
UPDATE accounts SET user_balance = user_balance - 1000 WHERE user_id = 1;
UPDATE accounts SET user_balance = user_balance + 1000 WHERE user_id = 2;

-- Apstiprinām izmaiņas
COMMIT;
```

1. **Sākums:** `START TRANSACTION;`
2. **Apstiprināšana:** `COMMIT;` – saglabā visas izmaiņas.
3. **Atcelšana:** `ROLLBACK;` – atgriež datubāzi sākotnējā stāvoklī.

Ja serveris pēkšņi apstājas, nepabeigtas transakcijas tiek **automātiski atceltas**.

#### Saglabāšanas punkti (SAVEPOINT)

Dažkārt nepieciešams **atgriezties uz konkrētu posmu**, nevis atcelt visu transakciju.

```sql
START TRANSACTION;

SAVEPOINT before_user1;
UPDATE accounts SET balance = balance + 100 WHERE user_id = 1;

-- Notiek pārbaude... ja nav veiksmīga:
ROLLBACK TO SAVEPOINT before_user1;

-- Turpinām ar otru lietotāju
UPDATE accounts SET balance = balance + 200 WHERE user_id = 2;

COMMIT;
```

- `SAVEPOINT` tikai **atzīmē pozīciju**, bet nesaglabā izmaiņas.
- Tikai `COMMIT` padara izmaiņas pastāvīgas.
- `ROLLBACK` bez `TO SAVEPOINT` atceļ visu transakciju un ignorē punktus.

---
### ⇄ Saistības
Avots >>> [Создание транзакций — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/creating-transactions)
Iepriekšēja lapa >>> [[Transakcijas]]
Nākama lapa >>> [[Navigācija - SQL]]
___