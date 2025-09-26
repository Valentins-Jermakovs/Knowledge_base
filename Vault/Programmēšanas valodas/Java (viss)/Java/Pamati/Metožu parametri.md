___

**Datums:** 2025-09-06
**Laiks:** 22:00
❚ **Tagi:** #java 

---
### Metožu parametri

Metodēm var nodot parametrus, re pāris piemēru:

Piemērs ar divu skaitļu nodošanu metodei:

```java
public class Program{
      
    public static void main (String args[]){
          
        int a = 6;
        int b = 8;
        sum(a, b);  // 14
        sum(3, a);  // 9
        sum(5, 23); // 28
    }
    static void sum(int x, int y){
         
        int z = x + y;
        System.out.println(z);
    }
}
```

String virknes nodošana metodei:

```java
public class Program{
      
    public static void main (String args[]){
          
        display("Tom", 34);
        display("Bob", 28);
        display("Sam", 23);
    }
    static void display(String name, int age){
         
        System.out.println(name);
        System.out.println(age);
    }
}
```

#### Nenoteikrs parametru daudzums

Šāds parametrs ļauj nodot nenoteiktu parametru daudzumu:

```java
public class Program{
      
    public static void main (String args[]){
          
        sum(1, 2, 3);           // 6
        sum(1, 2, 3, 4, 5);     // 15
        sum();                  // 0
    }
    static void sum(int ...nums){
         
        int result =0;
        for(int n: nums)
            result += n;
        System.out.println(result);
    }
}
```

```java
public static void main(String[] args) {
         
    sum("Welcome!", 20,10);
    sum("Hello World!");
}
static void sum(String message, int ...nums){
         
    System.out.println(message);   
    int result =0;
    for(int x:nums)
        result+=x;
    System.out.println(result);
}
```

---
### ⇄ Saistības

Avots >>> [Java \| Параметры методов](https://metanit.com/java/tutorial/2.16.php)
Iepriekšēja lapa >>> [[Programmēšanas valodas/Java (viss)/Java/Pamati/Metodes|Metodes]]
Nākama lapa >>> [[Operators return]]

---