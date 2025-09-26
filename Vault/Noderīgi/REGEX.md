___

**Datums:** 2025-07-02   
**Laiks:** 17:47 
❚ **Tagi:** #Noderīgi 
⌬ **Kurss:**  `Noderīgi`

---
### ⬢ Detalizēts apraksts
#### Regulāri izteikumi

> [!NOTE] REGEX
> REGEX (jeb regulārā izteiksme) ir veidne, ko var izmantot, lai atrastu, pārbaudītu vai aizstātu tekstu saskaņā ar noteiktiem noteikumiem.

To izmanto programmēšanā, strādājot ar teksta failiem, HTML, meklējot un aizstājot, kā arī validējot datus (piemēram, e-pastu, tālruņu numurus).

`\` ļauj ekranēt speciālos simbolus.

#### Sintakses pamati

| Sintakse | Nozīme                              | Piemērs                                |
| -------- | ----------------------------------- | -------------------------------------- |
| `.`      | Jebkurš simbols                     | `a.b` → `acb`, `a1b`                   |
| `^`      | Rindas sākums                       | `^abc` — строка начинается с `abc`     |
| `$`      | Rindas beigas                       | `abc$` — строка заканчивается на `abc` |
| `\d`     | Cipars (0-9)                        | `\d\d` → `23`, `01`                    |
| `\w`     | Burts, cipars                       | `\w\w` → `ab`, `A1`                    |
| `\s`     | Space, Tabs, jaunā rinda            | `\s` → `' '`, `\t`                     |
| `[abc]`  | Viens no simboliem `a`, `b` vai `c` | `[aeiou]` — гласные                    |
| `[^abc]` | Viss, izņemot `a`, `b`, `c`         | `[^0-9]` — не цифра                    |
| `[a-z]`  | Diapazons, no `a` līdz `z`          | `[A-Z]` — заглавные                    |
| a\|b     | `a` vai `b`                         | Или `a`, или `b`                       |
| `*`      | 0 un vairāk sakritību               | `a*` — `""`, `a`, `aaa`                |
| `+`      | Sakritību 1 vai vairāk reizes       | `a+` — `a`, `aa`                       |
| `?`      | Sakritība 0 vai 1 reizi             | `colou?r` → `color` и `colour`         |
| `{n}`    | Atkārtojums tieši `n` reizes        | `\d{3}` → `123`                        |
| `{n,}`   | `n` un vairāk atkārtojumu           | `a{2,}` — `aa`, `aaa`                  |
| `{n,m}`  | No `n` min līdz `m` max atkārtojumu | `\d{2,4}` — `12`, `123`, `1234`        |
| `()`     | Grupēšana                           | `(ab)+` — `ab`, `abab`                 |
![[7yvj6ajy-4i-2.jpg]]
#### Parastie piemēri

**E-pasta validācija**
```
^[\w-\.]+@([\w-]+\.)+[\w-]{2,4}$
```

**Telefona numura validācija**
```
 ^[\+]?[(]?[0-9]{3}[)]?[-\s\.]?[0-9]{3}[-\s\.]?[0-9]{4,6}$ 
```

**Paroles validācija**
```
 ^(?=.*?[A-Z])(?=.*?[a-z])(?=.*?[0-9])(?=.*?[#?!@$ %^&*-]).{8,}$ 
```

---
### ⇄ Saistības

Avoti:

- [Регулярные выражения. Часть 1 - Системный Блокъ](https://sysblok.ru/courses/regulyarnie-virazhenia-chast-1/)
- [Регулярные выражения. Часть 2 - Системный Блокъ](https://sysblok.ru/courses/reguljarnye-vyrazhenija-chast-2/)
- [Регулярные выражения. Часть 3 - Системный Блокъ](https://sysblok.ru/courses/reguljarnye-vyrazhenija-chast-3/)

Iepriekšēja lapa >>> [[Navigācija - Noderīgi]]

___