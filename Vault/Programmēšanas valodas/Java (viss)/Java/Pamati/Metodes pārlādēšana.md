___

**Datums:** 2025-09-06
**Laiks:** 22:08
❚ **Tagi:** #java 

---
### Metodes pārlādēšana

Programmā mēs varam izmantot metodes ar vienādu nosaukumu, bet ar dažādiem parametru tipiem un/vai skaitu. Šo mehānismu sauc par **metožu pārlādēšanu**:

```java
public class Program{
      
    public static void main(String[] args) {
         
        System.out.println(sum(2, 3));          // 5
        System.out.println(sum(4.5, 3.2));      // 7.7
        System.out.println(sum(4, 3, 7));       // 14
    }
    static int sum(int x, int y){
             
        return x + y;
    }
    static double sum(double x, double y){
             
        return x + y;
    }
    static int sum(int x, int y, int z){
             
        return x + y + z;
    }
}
```

---
### ⇄ Saistības

Avots >>> [Java \| Перегрузка методов](https://metanit.com/java/tutorial/2.18.php)
Iepriekšēja lapa >>> [[Operators return]]
Nākama lapa >>> [[Programmēšanas valodas/Java (viss)/Java/Pamati/Rekursīvas funkcijas|Rekursīvas funkcijas]]

---