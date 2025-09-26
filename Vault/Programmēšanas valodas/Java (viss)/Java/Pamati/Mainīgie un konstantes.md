___

**Datums:** 2025-09-06
**Laiks:** 18:31
❚ **Tagi:** #java 

---
### Mainīgie un konstantes

Mainīgo definēšana notiek šādā veidā:

```java
// mainīga_tips mainīgā_nosaukums;
int x;
```

#### Mainīgo inicializācija

Pastāv vairāki inicializācijas veidi:

- Pirmais:

```java
int x;      // объявление переменной
x = 10;     // присвоение значения
System.out.println(x);  // 10
```

- Otrais:

```java
int x = 10;     // объявление и инициализация переменной
System.out.println(x);  // 10
```

- Trešais (definējam mainīgos caur komatu un pēc tam inicializējam):

```java
int x, y;
x = 10;
y = 25;
System.out.println(x);  // 10
System.out.println(y);  // 25
```

- Ceturtais (definējam un inicializējam uzreiz):

```java
int x = 8, y = 15;
System.out.println(x);  // 8
System.out.println(y);  // 15
```

Programmas gaitā mainīgo vērtības var mainīt:

```java
int x = 10;
System.out.println(x);  // 10
x = 25;
System.out.println(x);  // 25
```

#### Atslēgas vārds `var`

Pastāv tāds mainīga tips, kā `var`, kas automātiski nosaka sev datu tipu, bet to vajag inicializēt uzreiz!

```java
var x = 10;
System.out.println(x);  // 10
```

#### Konstantes

Konstantes rakstā lielā reģistrā un atslēgvārds to definēšanai ir `final`:

```java
final int LIMIT = 5;
System.out.println(LIMIT);  // 5
// LIMIT=57; // так мы уже не можем написать, так как LIMIT - константа
```

Konstantes vērtība nav maināma, to vajag inicianalizēt uzreiz.

---
### ⇄ Saistības

Avots >>> [Java \| Переменные и константы](https://metanit.com/java/tutorial/2.1.php)
Iepriekšēja lapa >>> [[Programmēšanas valodas/Java (viss)/Java/Pamati/Komentāri|Komentāri]]
Nākama lapa >>> [[Programmēšanas valodas/Java (viss)/Java/Pamati/Datu tipi|Datu tipi]]

---