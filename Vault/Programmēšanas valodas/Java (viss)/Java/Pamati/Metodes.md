___

**Datums:** 2025-09-06
**Laiks:** 21:51
❚ **Tagi:** #java 

---
### Metodes

Kopēja struktūra metodēm ir šāda:

```
[modifikatori] atgriežamais_datu_tips metodes_nosaukums (parametri){
    // metodes ķermenis
}
```

Nedaudz par modifikatoriem:

> [!NOTE] static
> Java valodā static ir modifikators, kas norāda, ka klases elements (mainīgais, metode, ligzdota klase vai bloks) pieder pašai klasei, nevis tās konkrētam gadījumam (objektam).

> [!NOTE] public
> Šis te norāda, kā metode, klase ir pieejama visur.

Piemērs ar metodēm vienas klases ietvaros:

```java
public class Program{
      
    public static void main (String args[]){
         // šeit šīs metodes tiek izsauktas 
         hello();
         welcome();
         welcome();
    }
    // šeit tiek aprakstītas metodes
    static void hello(){
         
        System.out.println("Hello");
    }
    static void welcome(){
         
        System.out.println("Welcome to Java 10");
    }
}
```

---
### ⇄ Saistības

Avots >>> [Java \| Методы](https://metanit.com/java/tutorial/2.7.php)
Iepriekšēja lapa >>> [[Iterēšana pa daudzdimensiju masīviem]]
Nākama lapa >>> [[Metožu parametri]]

---