___

**Datums:** 2025-09-06
**Laiks:** 22:15
❚ **Tagi:** #java 

---
### Kļūdu, izņēmumu apstrāde

Java valodā kļūdu apstrāde notiek konstrukcijā `try...cath...finally`, kur:

- `try` - bloks, kurā tiek aprakstīts kods, kas potenciāli var izraisīt kļūdu;
- `cath` - bloks/i, kas apstrādā kļūdu vai kļūdas;
- `finally` - bloks, kas izpildās visos gadījumos.

Operators `throw` ļauj veidot savu kļūdu, nosacīti tiek nodots tekst objektam, ko var izvadīt un apstrādāt.

```java
try{
    int[] numbers = new int[3];
    numbers[4]=45;
    System.out.println(numbers[4]);
}
catch(Exception ex){
     
    ex.printStackTrace();
}
finally{
    System.out.println("Блок finally");
}
System.out.println("Программа завершена");
```

```java
int[] numbers = new int[3];
try{
    numbers[6]=45;
    numbers[6]=Integer.parseInt("gfd");
}
catch(ArrayIndexOutOfBoundsException ex){
             
    System.out.println("Выход за пределы массива");
}
catch(NumberFormatException ex){
             
    System.out.println("Ошибка преобразования из строки в число");
}
```

```java
package firstapp;
 
import java.util.Scanner;
public class FirstApp {
 
    public static void main(String[] args) {
        
        try{
            Scanner in = new Scanner(System.in);
            int x = in.nextInt();
            if(x>=30){
               throw new Exception("Число х должно быть меньше 30");
           }
        }
        catch(Exception ex){
             
            System.out.println(ex.getMessage());
        }
        System.out.println("Программа завершена");
    }   
}
```

---
### ⇄ Saistības

Avots >>> [Введение в обработку исключений \| Java](https://metanit.com/java/tutorial/2.10.php)
Iepriekšēja lapa >>> [[Programmēšanas valodas/Java (viss)/Java/Pamati/Rekursīvas funkcijas|Rekursīvas funkcijas]]
Nākama lapa >>> [[Programmēšanas valodas/Java (viss)/Java/Navigācija - Java]]

---