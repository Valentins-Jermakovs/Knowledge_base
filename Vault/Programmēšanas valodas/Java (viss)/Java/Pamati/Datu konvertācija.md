___

**Datums:** 2025-09-06
**Laiks:** 20:22
❚ **Tagi:** #java 

---
### Datu konvertācija

Java valodā pastāv tipu pārveidošana, līdzīga lieta ir `C#` valodai:

```java
int a = 4;
byte b = (byte)a;  // преобразование типов: от типа int к типу byte
System.out.println(b); // 4
```

Java valodā ir arī automātiska datu konvertācija:

![[Pasted image 20250906202923.png]]

Ar raustītu bultiņu parādīta tā konvertācija, kur datiem zūd precizitāte.

Lai nezaudēt datu precizitāti konvertācijas procesā, izmanto noapaļošanu, kas ir Javas matemātikas bibliotēkā:

```java
double a = 56.9898;
int b = (int)Math.round(a);
```

---
### ⇄ Saistības

Avots >>> [Java \| Преобразования типов данных](https://metanit.com/java/tutorial/2.2.php)
Iepriekšēja lapa >>> [[Piešķiršanas un kombinētie operatori]]
Nākama lapa >>> [[Konstrukcijas if, else]]

---