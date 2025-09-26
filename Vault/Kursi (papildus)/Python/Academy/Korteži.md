___

**Datums:** 2025-07-04   
**Laiks:** 10:25 
❚ **Tagi:** #Python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Kas tas ir?

> [!NOTE] Kortežs
> Python valodā kortežs ir sakārtota, nemaināma elementu kolekcija, kas var būt dažādu tipu. Vienkārši sakot, tas ir kā saraksts, bet tāds, ko pēc izveides nevar modificēt.

#### Korteža izveide

##### Izveide ar `()`

```python
# Пустой кортеж
empty_tuple = ()

# Кортеж с одним элементом (обязательно с запятой!)
single_item = (42,)
type(single_item)
# <class 'tuple'>

# Без запятой будет просто число: (42) == 42
single_item_num = (42)
type(single_item_num)
# <class 'int'>

# Кортеж чисел
numbers = (1, 2, 3, 4, 5)

# Кортеж с разными типами данных
mixed = (1, "hello", True, 3.14)

# Вложенные кортежи
nested = ((1, 2), ("a", "b"), (True, False))
```

##### Izveide caur komatiem

```python
# Создание кортежа без скобок
coordinates = 10.5, 20.7, 30.9
type(coordinates)
# <class 'tuple'>

# Распаковка кортежа
x, y, z = coordinates
print(x, y, z)
# 10.5 20.7 30.9
```

##### Izveide ar konstruktoru `tuple()`

```python
# Создание пустого кортежа
empty_tuple = tuple()

# Преобразование списка в кортеж
list_to_tuple = tuple([1, 2, 3])
print(list_to_tuple)
# (1, 2, 3)

# Преобразование строки в кортеж (каждый символ становится элементом)
string_to_tuple = tuple("Python")
print(string_to_tuple)
# ('P', 'y', 't', 'h', 'o', 'n')

# Преобразование множества в кортеж
set_to_tuple = tuple({1, 2, 3})
print(set_to_tuple)
# (1, 2, 3)
```

#### Pieeja pie korteža elementiem

##### Indeksācija

```python
fruits = ("apple", "banana", "cherry", "date", "elderberry")

# Получение элементов по индексу
first_fruit = fruits[0]
print(first_fruit)
# apple

# Отрицательные индексы для доступа с конца кортежа
last_fruit = fruits[-1]
print(last_fruit)
# elderberry
```

##### Griezumi (slices)

```python
fruits = ("apple", "banana", "cherry", "date", "elderberry")

# Первые три элемента
first_three = fruits[:3]
print(first_three)
# ('apple', 'banana', 'cherry')

# От второго до четвертого
middle = fruits[1:4]
print(middle)
# ('banana', 'cherry', 'date')

# Разворот кортежа
reversed_tuple = fruits[::-1]
print(reversed_tuple)
# ('elderberry', 'date', 'cherry', 'banana', 'apple')
```

##### Metodes

Tā kā korteži nav maināmi, pastāv tikai 2 metodes.

```python
fruits = ("apple", "banana", "cherry", "banana", "date")

# Подсчет количества вхождений элемента
banana_count = fruits.count("banana")
print(banana_count)


# Поиск индекса первого вхождения элемента
banana_index = fruits.index("banana")
print(banana_index)
```

#### Operācijas ar kortežiem

```python
# Узнать длину
fruits = ("apple", "banana", "cherry")
print(len(fruits))
# 3

# Проверить наличие элемента
print("apple" in fruits)
# True
print("mango" in fruits)
# False

# Конкатенация (объединение) кортежей
more_fruits = ("pear", "orange")
all_fruits = fruits + more_fruits
print(all_fruits)
# ('apple', 'banana', 'cherry', 'pear', 'orange')

# Повторение
repeated = fruits * 2
print(repeated)
# ('apple', 'banana', 'cherry', 'apple', 'banana', 'cherry')

# Распаковка
a, b, c = fruits
print(a, b, c)
# apple banana cherry
```

#### Praktiskie piemēri

##### 1. Vairāku vērtību atgriešana no funkcijas

```python
def get_user_info():
    name = "Anna"
    age = 30
    is_admin = True
    return name, age, is_admin

# Распаковка результата
user_name, user_age, user_is_admin = get_user_info()
print(f"Name: {user_name}, Age: {user_age}, Admin: {user_is_admin}")
# Name: Anna, Age: 30, Admin: True
```

##### 2. Fiksētie dati

```python
# Дни недели - идеальный пример неизменяемой последовательности
DAYS_OF_WEEK = ("Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday")

# Использование
today_index = 4  # Friday
print(f"Today is {DAYS_OF_WEEK[today_index]}")
# Today is Friday
```

#### Salīdzinājums

| Raksturlielums            | Saraksts (list)                        | Kortežs (tuple)        |
| ------------------------- | -------------------------------------- | ---------------------- |
| Sintakse                  | `[1, 2, 3]`                            | `(1, 2, 3)`            |
| Mainīgums                 | Jā                                     | Nē                     |
| Metodes                   | Daudzas: `append`, `remove`, `sort`... | Tikai `count`, `index` |
| Veiktspēja                | Lēnāka                                 | Ātrāka                 |
| Atmiņas izmantošana       | Lielāka                                | Mazāka                 |
| Var būt vārdnīcas atslēga | Nē                                     | Jā                     |
| Piemērots                 | Kolekcijām, kas var mainīties          | Nemainīgiem datiem     |

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Saraksta ģenerators]]
Nākama lapa >>> [[Kopas]]

---
### ⇄ Saistības
Avots >>> [Кортежи — Интерактивный курс по Python](https://python-academy.org/ru/guide/tuples)
Iepriekšēja lapa >>> [[Kursi (papildus)/Python/Academy/Saraksti]]
Nākama lapa >>> [[Kopas]]

___