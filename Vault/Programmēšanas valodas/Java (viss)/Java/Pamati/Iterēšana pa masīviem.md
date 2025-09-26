___

**Datums:** 2025-09-06
**Laiks:** 21:36
❚ **Tagi:** #java 

---
### Iterēšana pa masīviem

Iterēt pa masīvu var caur standarta `for` ciklu, vai tā paveidu, kas pēc būtības līdzīgs `foreach` ciklam citās valodās.

Piemērs ar parasto `for` ciklu:

```java
int[] array = new int[] { 1, 2, 3, 4, 5 };
for (int i=0; i<array.length;i++){
    array[i] = array[i] * 2;
    System.out.println(array[i]);
}
/*
2
4
6
8
10
*/
```

Piemērs ar `foreach` paveidu:

```java
int[] array = new int[] { 1, 2, 3, 4, 5 };
for (int i : array){
             
    System.out.println(i);
}
/*
1
2
3
4
5
*/
```

---
### ⇄ Saistības

Avots >>> [Java \| Массивы](https://metanit.com/java/tutorial/2.4.php)
Iepriekšēja lapa >>> [[Zobrata masīvs]]
Nākama lapa >>> [[Iterēšana pa daudzdimensiju masīviem]]

---