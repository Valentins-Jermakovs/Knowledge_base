___

**Datums:** 2025-07-30   
**Laiks:** 12:53 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Modulis

Modulis `random` atbild par nejaušo skaitļu ģenerēšanu.

| Metode        | Ko dara                                       |
| ------------- | --------------------------------------------- |
| `random()`    | ģenerē skaitli no `0.0` līdz `1.0`            |
| `randint()`   | atgriež nejaušo skaitli no norādīta diapazona |
| `randrange()` | atgriež nejaušo skaitli no skaitļu komplekta  |
| `shuffle()`   | sajauc sarakstu                               |
| `choice()`    | atgriež nejaušo skaitli no saraksta           |
#### Piemēri

##### Metode `random()`

```python
import random
 
number = random.random()  # значение от 0.0 до 1.0
print(number)
number = random.random() * 100  # значение от 0.0 до 100.0
print(number)
```

##### Metode `randint()`

```python
import random
 
number = random.randint(20, 35)  # значение от 20 до 35
print(number)
```

##### Metode `randrange()`

```python
import random
 
number = random.randrange(10)  # значение от 0 до 10 не включая
print(number)
number = random.randrange(2, 10)  # значение в диапазоне 2, 3, 4, 5, 6, 7, 8, 9
print(number)
number = random.randrange(2, 10, 2)  # значение в диапазоне 2, 4, 6, 8
print(number)
```

##### Darbs ar sarakstiem

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8]
random.shuffle(numbers) # sajauc sarakstu
print(numbers)  
random_number = random.choice(numbers) # atgriež kādu saraksta elementu
print(random_number)
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Modulis string]]
Nākama lapa >>> [[Modulis secrets]]

---
### ⇄ Saistības

Avots >>> [Python \| Модуль random](https://metanit.com/python/tutorial/6.1.php)
Iepriekšēja lapa >>> [[Modulis]]
Nākama lapa >>> [[Modulis secrets]]

___