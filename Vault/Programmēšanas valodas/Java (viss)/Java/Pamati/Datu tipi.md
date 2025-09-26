___

**Datums:** 2025-09-06
**Laiks:** 18:40
❚ **Tagi:** #java 

---
### Datu tipi

Zemāk ir datu tipu tabula. Java valodā ir daudz savu nianšu mainīgo inicializācijā, ko var apskatīt piemēros:

| Tips        | Apraksts (latviski)                                                                                        | Īpatnības deklarācijā                                                                      | Piemērs                                               |
| ----------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | ----------------------------------------------------- |
| **boolean** | Glabā tikai divas loģiskās vērtības: `true` vai `false`.                                                   | Noklusējuma vērtība `false`. Izmanto loģiskos izteikumos.                                  | `boolean isActive = false;` `boolean isAlive = true;` |
| **byte**    | Vesels skaitlis diapazonā no **-128** līdz **127**.                                                        | Lieto, ja vajag ietaupīt atmiņu. Var pāriet pāri robežām (pārplūde).                       | `byte a = 3;` `byte b = 8;`                           |
| **short**   | Vesels skaitlis diapazonā no **-32,768** līdz **32,767**.                                                  | Mazliet plašāks par `byte`, bet retāk izmanto.                                             | `short a = 3;` `short b = 8;`                         |
| **int**     | Vesels skaitlis diapazonā no **-2,147,483,648** līdz **2,147,483,647**.                                    | Noklusējuma tips veseliem skaitļiem.                                                       | `int a = 4;` `int b = 9;`                             |
| **long**    | Ļoti liels vesels skaitlis diapazonā no **-9,223,372,036,854,775,808** līdz **9,223,372,036,854,775,807**. | Literāļiem jābeidzas ar `L` vai `l`.                                                       | `long a = 5L;` `long b = 10L;`                        |
| **double**  | Skaitlis ar peldošo komatu (dubultā precizitāte). Aptuvenais diapazons: ±4.9 * 10⁻³²⁴ līdz ±1.797 * 10³⁰⁸. | Noklusējuma tips peldošajiem skaitļiem. Decimāldaļas atdalīšanai izmanto **punktu** (`.`). | `double x = 8.5;` `double y = 2.7;`                   |
| **float**   | Skaitlis ar peldošo komatu (vienkārša precizitāte). Aptuvenais diapazons: ±3.4 * 10³⁸.                     | Literāļiem obligāti jāpievieno `F` vai `f`.                                                | `float x = 8.5F;` `float y = 2.7F;`                   |
| **char**    | Viens simbols (UTF-16 kodējums). Diapazons: no **0** līdz **65,535**.                                      | Apzīmē ar vienpēdiņām `' '`. Var glabāt arī skaitlisko Unicode vērtību.                    | `char c = 'A';` `char d = 97;`                        |

#### String datu tips

Šādi iskatās `String` tipa mainīgo inicializācija, `\n` apzīmē pārēju uz jauno rindu:

```java
String text = "Hello \nworld";
System.out.println(text);

// Hello 
// world
```

Ir ieviests arī teksta bloku atbalsts:

```java
String text = "Вот мысль, которой весь я предан,\n"+
                "Итог всего, что ум скопил.\n"+
                "Лишь тот, кем бой за жизнь изведан,\n"+
                "Жизнь и свободу заслужил.";
System.out.println(text);

/*
Вот мысль, которой весь я предан,
Итог всего, что ум скопил.
Лишь тот, кем бой за жизнь изведан,
Жизнь и свободу заслужил.
*/
```

---
### ⇄ Saistības

Avots >>> [Java \| Типы данных](https://metanit.com/java/tutorial/2.12.php)
Iepriekšēja lapa >>> [[Mainīgie un konstantes]]
Nākama lapa >>> [[Programmēšanas valodas/Java (viss)/Java/Pamati/Konsoles izvads|Konsoles izvads]]

---