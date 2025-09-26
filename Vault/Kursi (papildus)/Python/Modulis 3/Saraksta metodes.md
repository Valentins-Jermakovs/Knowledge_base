___

**Datums:** 2025-07-27   
**Laiks:** 13:24 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Saraksta metodes

##### `.append()`

Metode `append()` ļauj pievienot elementu saraksta beigās.

```python
my_list = [1, 2]
my_list.append(3)
```

Pie saraksta var pievienot arī vārdnīcas:

```python
expenses.append({'amount': amount})
expenses.append({'category': category})
# or
expenses.append({'amount': amount, 'category': category})
```

##### `.insert()`

Metode `insert()` ļauj ievietot elementu norādītā pozīcijā.

```python
example_list = [4, 5, 6, 7]
example_list.insert(2, 5.5)

print(example_list) # [4, 5, 5.5, 6, 7]
```

Kur:

- `2` - indekss, pozīcija, kur ievietot jauno elementu;
- `5.5` - vērtība, kas tiks ievietota.

##### `.pop()`

Metode `pop()` ļauj izdzēst elementu no saraksta, kā no konkrētas pozīcijas, tā arī pēdējo elementu, ja parametrs netiek norādīts.

```python
fruits_list = ["cherry", "lemon", "tomato", "apple", "orange"]

fruits_list.pop(2)

print(fruits_list) # ["cherry", "lemon", "apple", "orange"]
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Saraksts]]
Nākama lapa >>> [[Saraksta izveide no for cikla]]

---
### ⇄ Saistības

Avots >>> [freecodecamp.org/learn/scientific-computing-with-python/learn-lambda-functions-by-building-an-expense-tracker/step-3](https://www.freecodecamp.org/learn/scientific-computing-with-python/learn-lambda-functions-by-building-an-expense-tracker/step-3)
Iepriekšēja lapa >>> [[Saraksts]]
Nākama lapa >>> [[Kursi (papildus)/Python/Modulis 3/Vārdnīcas]]

___