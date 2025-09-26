___

**Datums:** 2025-09-06
**Laiks:** 20:59
❚ **Tagi:** #java 

---
### Masīvi

Java valodā masīvs glabā tikai sava datu tipa elementus!

Java valodā masīvus var definēt, inicializēt divos veidos:

- sākumā veidojam tukšo masīvu:

```java
int nums[];
nums = new int[4];  // ierezervējam atmiņu 4 elementiem
```

```java
int nums[] = new int[4];    // masīvs no 4 elementiem
int[] nums2 = new int[5];   // masīvs no 5 elementiem
```

- definējam un uzreiz inicializējam masīvus:

```java
// abi veidi ir vienlīdzīgi
int[] nums = new int[] { 1, 2, 3, 5 };
 
int[] nums2 = { 1, 2, 3, 5 };
```

Ja mēs izmantojam pirmo pieeju, kad tiek veidots tukšs masīvs ar konkrētu elementu daudzumu, tad tā elementus var inicializēt caur indeksiem:

```java
int[] nums = new int[4];
// устанавливаем значения элементов массива
nums[0] = 1;
nums[1] = 2;
nums[2] = 4;
nums[3] = 100;
         
// получаем значение третьего элемента массива
System.out.println(nums[2]);    // 4
```

---
### ⇄ Saistības

Avots >>> [Java \| Массивы](https://metanit.com/java/tutorial/2.4.php)
Iepriekšēja lapa >>> [[Operatori continue un break]]
Nākama lapa >>> [[Masīva garums]]

---