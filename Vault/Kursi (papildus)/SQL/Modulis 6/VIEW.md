___
**Datums:** 2025-07-02   
**Laiks:** 13:27 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Skats

> [!NOTE] Skats
> Skats ir datubāzes objekts, kas rodas, izpildot datubāzes vaicājumu, kas definēts, izmantojot `SELECT` operatoru, skata piekļuves brīdī.

Skatus dažreiz sauc par "virtuālām tabulām". Tas ir tāpēc, ka skats lietotājam tiek parādīts kā tabula, bet faktiski nesaglabā datus. Tas izgūst datus no citām tabulām, kad tam piekļūst.

```sql
CREATE VIEW ViewUsers AS
    SELECT id,
           name,
           CONCAT(SUBSTR(email, 1, 2), '****', SUBSTR(email, -4)) AS email
FROM Users;
```

Pec izveides šādus skatus var izmantot nākotnē, piem., apskatīt:

```sql
SELECT * FROM ViewUsers;
```

Kā arī apskatīt, kādas kolonnas ir iekļautas skatā:

```sql
DESCRIBE ViewUsers;
```

#### Skata vispārīga sintakse

```sql
CREATE [OR REPLACE]
VIEW имя_представления [(имена_полей_представления)]
AS select_выражение
```

`OR REPLACE` - Izmantojot šo neobligāto parametru, ja jau pastāv skats ar tādu pašu nosaukumu, vecais skats tiks izdzēsts un izveidots jauns. Pretējā gadījumā, mēģinot izveidot skatu ar esošu nosaukumu, radīsies kļūda.

---
### ⇄ Saistības
Avots >>> [Представления, VIEW — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/view)
Iepriekšēja lapa >>> [[Datuma un laika tipi]]
Nākama lapa >>> [[Indeksi]]
___