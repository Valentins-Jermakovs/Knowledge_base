___

**Datums:** 2025-09-06
**Laiks:** 19:06
❚ **Tagi:** #java 

---
### Konsoles ievads

Java valodā konsoles ievada iegūšanai izmanto klasi `Scanner` un objektu `in`:

```java
import java.util.Scanner;
 
public class Program {
   
    public static void main(String[] args) {
           
        Scanner in = new Scanner(System.in); // atvēr kosnoles ievadu
        System.out.print("Input a number: ");
        int num = in.nextInt();
          
        System.out.printf("Your number: %d \n", num);
        in.close(); // aizver konsoles ievadu
    }
}
```

Priekš ievada izveidošanas obligāti importē `Scanner` un tad veido objektu, kas tiks izmantots ievada nolasīšanai.

Lai iegūt lietotāja ievadu, izmanto šādas `in` objekta metodes:

| Metode            | Apraksts                                          |
| ----------------- | ------------------------------------------------- |
| **next()**        | Nolasa ievadīto tekstu līdz pirmajai atstarpei    |
| **nextLine()**    | Nolasa visu ievadīto rindu (līdz jaunajai rindai) |
| **nextInt()**     | Nolasa veselu skaitli (`int`)                     |
| **nextDouble()**  | Nolasa skaitli ar peldošo komatu (`double`)       |
| **nextBoolean()** | Nolasa loģisko vērtību (`boolean`)                |
| **nextByte()**    | Nolasa veselu skaitli (`byte`)                    |
| **nextFloat()**   | Nolasa skaitli ar peldošo komatu (`float`)        |
| **nextShort()**   | Nolasa veselu skaitli (`short`)                   |


---
### ⇄ Saistības

Avots >>> [Java \| Консольный ввод-вывод](https://metanit.com/java/tutorial/2.9.php)
Iepriekšēja lapa >>> [[Programmēšanas valodas/Java (viss)/Java/Pamati/Konsoles izvads|Konsoles izvads]]
Nākama lapa >>> [[Aritmētiskas operācijas]]

---