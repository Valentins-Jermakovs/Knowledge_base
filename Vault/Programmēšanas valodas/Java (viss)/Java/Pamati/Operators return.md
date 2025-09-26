___

**Datums:** 2025-09-06
**Laiks:** 22:04
❚ **Tagi:** #java 

---
### Operators return

Operators retun ļauj atgriez skaitļošanu rezultātu no metodes:

```java
public class Program{
      
    public static void main (String args[]){
          
        int x = sum(1, 2, 3);
        int y = sum(1, 4, 9);
        System.out.println(x);  // 6
        System.out.println(y);  // 14
    }
    static int sum(int a, int b, int c){
         
        return a + b + c;
    }
}
```

#### Iziešana no `void` metodēm

Metodēm ar datu tipu `void` operators `return` var tikt izmantots, lai apstādināt funkcijas darbību, iziet no tās:

```java
public class Program{
      
    public static void main (String args[]){
          
        daytime(7);     // Good morning
        daytime(13);    // Good after noon
        daytime(32);    // 
        daytime(56);    // 
        daytime(2);     // Good night
    }
    static void daytime(int hour){
         
        if (hour >24 || hour < 0)
            return;
        if(hour > 21 || hour < 6)
            System.out.println("Good night");
        else if(hour >= 15)
            System.out.println("Good evening");
        else if(hour >= 11)
            System.out.println("Good after noon");
        else
            System.out.println("Good morning");
    }
}
```

---
### ⇄ Saistības

Avots >>> [Java \| Оператор return. Результат метода](https://metanit.com/java/tutorial/2.17.php)
Iepriekšēja lapa >>> [[Metožu parametri]]
Nākama lapa >>> [[Metodes pārlādēšana]]

---