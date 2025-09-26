___
**Datums:** 2025-06-27   
**Laiks:** 13:43 
❚ **Tagi:** #SQL 
⌬ **Kurss:**  `SQL`

---
### ⬢ Detalizēts apraksts
#### Tabulas struktūra
Relāciju DB dati tiek saglabāti saistītās savā starpā tabulās.
Pašas tabulas sastāv no:
- rindām (ko sauc par ierakstiem)
- kolonnām (ko sauc par atribūtiem)

Katrai kolonnai tiek piešķirts savs datu tips, piemēram:
- `VARCHAR` - teksta rinda
- `INTEGER` - skaitļi
- `DATETIME` - datu tips priekš datuma un laika

Lai uzzināt tabulas `atribūtu` datu tipus, var izmantot SQL komandu `DESCRIBE`.

```SQL
DESCRIBE tabulas_nosaukums
```

#### Primāra atslēga

> [!NOTE] Primāra atslēga
> Atslēgas lauks (primārā atslēga) ir lauks (vai lauku kopa), kura vērtība unikāli identificē katru tabulas ierakstu.

> Piezīme: Primāra atslēga nav visur obligāta, taču tās izmantošana ieteicama.
#### Ārēja atslēga

> [!NOTE] Ārēja atslēga
> Ārējā atslēga ir lauks (vai lauku kopa) vienā tabulā, kas atsaucas uz primāro atslēgu citā tabulā.

Tabulu <mark style="background: #FFB86CA6;">ar ārējo atslēgu</mark> sauc par <mark style="background: #FFB86CA6;">bērnu tabulu</mark>, bet tabulu <mark style="background: #ADCCFFA6;">ar primāro atslēgu</mark> - <mark style="background: #ADCCFFA6;">par atsauces vai vecāku tabulu.</mark>

![[ru_keys.webp]]

Primārā atslēga ir atbildīga par to, lai katrs ieraksts tabulā būtu unikāli identificēts. Ārējā atslēga ir atbildīga par atsauces integritāti.

---
### ⇄ Saistības
Avots >>> [Структура реляционных баз данных — Интерактивный курс по SQL](https://sql-academy.org/ru/guide/structure-of-relation-databases)
Iepriekšēja lapa >>> [[Dokumentu orientēta DB]]
Nākama lapa >>> [[Ievada informācija par SQL]]
___