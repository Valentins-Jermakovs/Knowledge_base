___

**Datums:** 2025-09-06
**Laiks:** 18:53
❚ **Tagi:** #java 

---
### Konsoles izvads

Java valodā ir 2 metodes, lai izvadīt informāciju konsolē:

- `System.out.println` - izvada un pievieno jauno rindu beigās;
- `System.out.print` - izvada, bet jauno rindu NELIEK.

Mainīgo izvadam teksta rindā var izmantot vienu no 2 pieejām.

Pirmais variants:

```java
public class Program {
   
    public static void main(String[] args) {
           
        int x=5;
        int y=6;
        System.out.println("x=" + x + "; y=" + y);
    }
}

// x=5; y=6
```

Otrais variants ir izmantot specifikātorus, ko var apskatīt tabulā:

| Specifikātors | Pielietojums                                             |
| ------------- | -------------------------------------------------------- |
| `%d`          | tiek izmantots veselu skaitļu izvadam                    |
| `%x`          | tiek izmantots heksadecimālu skaitļu izvadam             |
| `%f`          | tiek izmantots, lai izvadīt skaitļus ar komatu           |
| `%e`          | tiek izmantots, lai izvadīt skaitļus eksponenciālā formā |
| `%c`          | tiek izmantots viena simbola izvadam                     |
| `%s`          | tiek izmantots teksta rindu izvadam                      |
Specifikātoru pielietojuma piemērs:

```java
public class Program {
   
    public static void main(String[] args) {
           
        String name = "Tom";
        int age = 30;
        float height = 1.7f;
          
        System.out.printf("Name: %s  Age: %d  Height: %.2f \n", name, age, height);
    }
}
// Name: Tom  Age: 30  Height: 1,70
```

---
### ⇄ Saistības

Avots >>> [Java \| Консольный ввод-вывод](https://metanit.com/java/tutorial/2.9.php)
Iepriekšēja lapa >>> [[Programmēšanas valodas/Java (viss)/Java/Pamati/Datu tipi|Datu tipi]]
Nākama lapa >>> [[Konsoles ievads]]

---