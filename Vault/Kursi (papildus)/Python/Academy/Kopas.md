___

**Datums:** 2025-07-04   
**Laiks:** 10:47 
❚ **Tagi:** #Python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Kas ir kopas?

> [!NOTE] Kopa
> Kopa Python valodā ir nesakārtota unikālu elementu kolekcija.

#### Kopas izveide

##### Izveide ar `{}`

```python
# Множество целых чисел
numbers = {1, 2, 3, 4, 5}
print(numbers)
# {1, 2, 3, 4, 5}

# Автоматическое удаление дубликатов
duplicates = {1, 2, 2, 3, 3, 3, 4, 5, 5}
print(duplicates)
# {1, 2, 3, 4, 5}

# Множество с разными типами данных
mixed = {1, "привет", (1, 2, 3)}
print(mixed)
# {1, 'привет', (1, 2, 3)}
```

>Svarīgi. `{}` neļauj izveidot tukšo kopu. Lai izveidot tukšo kopu, izmanto `set()`.

##### Izveide ar konstruktoru `set()`

```python
# Пустое множество
empty_set = set()
print(empty_set)
# set()

# Создание множества из списка
numbers_set = set([1, 2, 2, 3, 4, 4, 5])
print(numbers_set)
# {1, 2, 3, 4, 5}

# Создание множества из строки
letters = set("hello")
print(letters)  # 'l' встречается только один раз
# {'h', 'e', 'l', 'o'}
```

##### Izveide ar ģeneratoru

```python
# Множество квадратов чисел от 0 до 9
squares = {x**2 for x in range(10)}
print(squares)
# {0, 1, 4, 9, 16, 25, 36, 49, 64, 81}
```

#### Pamata operācijas

##### Pārbaude uz elementa esamību

```python
fruits = {"яблоко", "банан", "вишня"}

print("яблоко" in fruits)
# True
print("груша" in fruits)
# False
```

##### Elementu pievienošana, dzēšana

```python
fruits = {"яблоко", "банан"}

# Добавление одного элемента
fruits.add("вишня")
print(fruits)
# {'яблоко', 'вишня', 'банан'}

# Добавление нескольких элементов
fruits.update(["груша", "апельсин"])
print(fruits)
# {'яблоко', 'вишня', 'банан', 'груша', 'апельсин'}

# Удаление элемента
fruits.remove("банан")  # вызывает KeyError, если элемента нет
print(fruits)
# {'яблоко', 'вишня', 'груша', 'апельсин'}

# Безопасное удаление элемента
fruits.discard("вишня")  # не вызывает ошибку, если элемента нет
print(fruits)
# {'яблоко', 'груша', 'апельсин'}

# Извлечение произвольного элемента
random_fruit = fruits.pop()
print(random_fruit)
# яблоко
print(fruits)
# {'груша', 'апельсин'}

# Очистка множества
fruits.clear()
print(fruits)
# set()
```

##### Iterācija pa elementiem

```python
colors = {"красный", "синий", "зеленый"}

for color in colors:
    print(color)
# красный
# синий
# зеленый
```

#### Matemātiskas operācijas

##### Apvienošana (Union)

```python
a = {1, 2, 3}
b = {3, 4, 5}

# С оператором |
union_set = a | b
print(union_set)
# {1, 2, 3, 4, 5}

# С методом union()
union_set = a.union(b)
print(union_set)
# {1, 2, 3, 4, 5}
```

##### Krustojums (Intersection)

```python
a = {1, 2, 3, 4}
b = {3, 4, 5, 6}

# С оператором &
intersection_set = a & b
print(intersection_set)
# {3, 4}

# С методом intersection()
intersection_set = a.intersection(b)
print(intersection_set)
# {3, 4}
```

##### Dažādība (Difference)

```python
a = {1, 2, 3, 4}
b = {3, 4, 5, 6}

# С оператором -
difference_set = a - b
print(difference_set)
# {1, 2}

# С методом difference()
difference_set = a.difference(b)
print(difference_set)
# {1, 2}
```

#### Salīdzināšanas operācijas

```python
a = {1, 2, 3}
b = {1, 2, 3, 4, 5}
c = {1, 2, 3}

# Равенство множеств
print(a == c)  # Содержат одинаковые элементы
# True

# Подмножества
print(a.issubset(b))  # Все элементы a есть в b
# True
print(a < b)  # a является строгим подмножеством b
# True

# Надмножества
print(b.issuperset(a))  # b содержит все элементы a
# True
print(b > a)  # b является строгим надмножеством a
# True

# Проверка на отсутствие общих элементов
d = {6, 7, 8}
print(a.isdisjoint(d))  # Нет общих элементов
# True
```

#### Nemaināma kopa `frozenset`

Izmantojot `frozenset()` var izveidot nemaināmo kopu, līdzīgi kortežam.

```python
# Создание frozenset
immutable_set = frozenset([1, 2, 3, 4])
print(immutable_set)
# frozenset({1, 2, 3, 4})

# Попытка изменить frozenset вызывает ошибку
try:
    immutable_set.add(5)
except AttributeError as e:
    print(f"Ошибка: {e}")
# Ошибка: 'frozenset' object has no attribute 'add'

# frozenset можно использовать как ключ словаря или элемент другого множества
normal_set = {frozenset([1, 2]), frozenset([3, 4])}
print(normal_set)
# {frozenset({1, 2}), frozenset({3, 4})}
```

#### Praktiskie piemēri

##### 1. Dublikātu dzēšana no saraksta

```python
numbers = [1, 2, 2, 3, 3, 3, 4, 5, 5]
unique_numbers = list(set(numbers))
print(unique_numbers)

# [1, 2, 3, 4, 5]
```

##### 2. Kopējo elementu meklēšana

```python
users_group1 = ["Анна", "Иван", "Мария", "Петр", "Елена"]
users_group2 = ["Иван", "Ольга", "Елена", "Алексей"]

# Общие элементы (пересечение)
common_users = set(users_group1) & set(users_group2)
print(f"Пользователи в обеих группах: {common_users}")
# Пользователи в обеих группах: {'Елена', 'Иван'}

# Элементы только из первой группы (разность)
only_group1 = set(users_group1) - set(users_group2)
print(f"Только в группе 1: {only_group1}")
# Только в группе 1: {'Мария', 'Анна', 'Петр'}

# Все уникальные элементы (объединение)
all_users = set(users_group1) | set(users_group2)
print(f"Все уникальные пользователи: {all_users}")
# Все уникальные пользователи: {'Елена', 'Иван', 'Мария', 'Анна', 'Ольга', 'Алексей', 'Петр'}
```

##### 3. Pārbaude uz unikāliem elementiem

```python
def are_all_unique(items):
    # Проверяет, все ли элементы в последовательности уникальны.
    return len(set(items)) == len(items)

print(are_all_unique([1, 2, 3, 4, 5]))
# True
print(are_all_unique([1, 2, 3, 3, 4]))
# False
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Korteži]]
Nākama lapa >>> [[Kursi (papildus)/Python/Academy/Vārdnīcas|Vārdnīcas]]

---
### ⇄ Saistības
Avots >>> [Множества — Интерактивный курс по Python](https://python-academy.org/ru/guide/sets)
Iepriekšēja lapa >>> [[Korteži]]
Nākama lapa >>> [[Kursi (papildus)/Python/Academy/Vārdnīcas]]

___