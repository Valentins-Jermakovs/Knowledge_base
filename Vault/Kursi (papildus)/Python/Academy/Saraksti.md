___
**Datums:** 2025-07-03   
**Laiks:** 18:25 
❚ **Tagi:** #Python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Saraksts

Sarakstu pamatīpašības:

- **Sakārtoti**: elementi tiek glabāti tādā secībā, kādā tie tika pievienoti.
- **Modificējami:** elementus var pievienot, noņemt un modificēt pēc saraksta izveides.
- **Indeksējami:** katram elementam var piekļūt pēc tā pozīcijas (indeksa).
- **Ļauj dublikātus:** viens un tas pats elements sarakstā var parādīties vairākas reizes.

#### Sarakstu izveide

##### Izveide ar `[]`

```python
# Пустой список
empty_list = []
print(empty_list)

# Список чисел
numbers = [1, 2, 3, 4, 5]
print(numbers)

# Список разных типов данных
mixed = [1, "привет", True, 3.14]
print(mixed)

# Вложенные списки (список списков)
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
print(matrix)
```

##### Izveide ar konstruktoru `list()`

```python
# Создание пустого списка
empty_list = list()
print(empty_list)
# []

# Создание списка из строки (каждый символ становится элементом)
chars = list("Python")
print(chars)
# ['P', 'y', 't', 'h', 'o', 'n']

# Создание списка из других итерируемых объектов
tuple_to_list = list((1, 2, 3))
print(tuple_to_list)
# [1, 2, 3]

set_to_list = list({1, 2, 3})
print(set_to_list)
# [1, 2, 3]
```

##### Izveide ar ģeneratoru
```python
# Создание списка квадратов чисел от 0 до 9
squares = [x**2 for x in range(10)]
print(squares)
# [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# Создание списка четных чисел от 0 до 9
even_numbers = [x for x in range(10) if x % 2 == 0]
print(even_numbers)
# [0, 2, 4, 6, 8]
```

#### Piekļuve pie saraksta elementiem

##### Indeksācija

```python
fruits = ["яблоко", "банан", "вишня", "груша", "апельсин"]

# Получение элементов по индексу
first_fruit = fruits[0]
print(f"Первый фрукт: {first_fruit}")
# Первый фрукт: яблоко

# Отрицательные индексы для доступа с конца списка
last_fruit = fruits[-1]
print(f"Последний фрукт: {last_fruit}")
# Последний фрукт: апельсин

second_last = fruits[-2]
print(f"Предпоследний фрукт: {second_last}")
# Предпоследний фрукт: груша
```

##### Griezumi (slices)

```python
fruits = ["яблоко", "банан", "вишня", "груша", "апельсин"]

# Синтаксис среза: список[начало:конец:шаг]
# Начало включается, конец не включается!

# Первые три элемента
first_three = fruits[0:3]
print(f"Первые три фрукта: {first_three}")
# Первые три фрукта: ['яблоко', 'банан', 'вишня']

# То же самое, но начальный индекс можно опустить, если он 0
first_three = fruits[:3]
print(f"Первые три фрукта: {first_three}")
# Первые три фрукта: ['яблоко', 'банан', 'вишня']

# Каждый второй элемент
every_second = fruits[::2]
print(f"Каждый второй фрукт: {every_second}")
# Каждый второй фрукт: ['яблоко', 'вишня', 'апельсин']

# Разворот списка
reversed_list = fruits[::-1]
print(f"Список в обратном порядке: {reversed_list}")
# Список в обратном порядке: ['апельсин', 'груша', 'вишня', 'банан', 'яблоко']
```

#### Elementu maiņa

```python
fruits = ["яблоко", "банан", "вишня"]

# Изменение элемента
fruits[0] = "киви"
print(fruits)
# ['киви', 'банан', 'вишня']

# Изменение нескольких элементов с помощью среза
numbers = [1, 2, 3, 4, 5]
numbers[1:4] = [20, 30, 40]
print(numbers)
# [1, 20, 30, 40, 5]

# Можно даже заменить несколько элементов на другое количество
numbers = [1, 2, 3, 4, 5]
numbers[1:4] = [20, 30]
print(numbers)
# [1, 20, 30, 5]
```

#### Sarakstu metodes

##### Elementu pievienošana

```python
fruits = ["яблоко", "банан"]

# Добавление элемента в конец списка
fruits.append("вишня")
print(fruits)
# ['яблоко', 'банан', 'вишня']

# Вставка элемента на определенную позицию
fruits.insert(1, "апельсин")
print(fruits)
# ['яблоко', 'апельсин', 'банан', 'вишня']

# Добавление элементов из другого списка
more_fruits = ["груша", "виноград"]
fruits.extend(more_fruits)
print(fruits)
# ['яблоко', 'апельсин', 'банан', 'вишня', 'груша', 'виноград']

# Объединение списков с помощью оператора +
combined = fruits + ["ананас", "манго"]
print(combined)
# ['яблоко', 'апельсин', 'банан', 'вишня', 'груша', 'виноград', 'ананас', 'манго']
```

##### Elementu dzēšana

```python
fruits = ["яблоко", "банан", "вишня", "апельсин", "банан"]

# Удаление элемента по значению (удаляет только первое вхождение)
fruits.remove("банан")
print(fruits)
# ['яблоко', 'вишня', 'апельсин', 'банан']

# Удаление элемента по индексу и возврат его значения
removed = fruits.pop(1)
print(f"Удален: {removed}")
# Удален: вишня
print(f"Список после удаления: {fruits}")
# Список после удаления: ['яблоко', 'апельсин', 'банан']

# Если индекс не указан, pop() удаляет и возвращает последний элемент
last = fruits.pop()
print(f"Последний элемент: {last}")
# Последний элемент: банан
print(fruits)
# ['яблоко', 'апельсин']

# Удаление всех элементов из списка
fruits.clear()
print(f"Пустой список: {fruits}")
# Пустой список: []

# Оператор del для удаления элементов по индексу или срезу
numbers = [1, 2, 3, 4, 5]
del numbers[0]
print(numbers)
# [2, 3, 4, 5]

del numbers[1:3]
print(numbers)
# [2, 5]
```

#### Elementu skaitīšana un meklēšana

```python
fruits = ["яблоко", "банан", "вишня", "банан", "груша"]

# Проверка наличия элемента в списке
print("банан" in fruits)
# True
print("арбуз" in fruits)
# False

# Поиск индекса первого вхождения элемента
banana_index = fruits.index("банан")
print(f"Индекс первого банана: {banana_index}")
# Индекс первого банана: 1

# Подсчет количества вхождений элемента
banana_count = fruits.count("банан")
print(f"Количество бананов: {banana_count}")
# Количество бананов: 2

print(len(fruits))
# 5
```

#### Saraksta kārtošana

```python
# Сортировка списка (изменяет исходный список)
numbers = [3, 1, 4, 1, 5, 9, 2]
numbers.sort()
print(f"Отсортированный список: {numbers}")
# Отсортированный список: [1, 1, 2, 3, 4, 5, 9]

# Сортировка в обратном порядке
numbers.sort(reverse=True)
print(f"Обратная сортировка: {numbers}")
# Обратная сортировка: [9, 5, 4, 3, 2, 1, 1]

# Если не хотите изменять исходный список, используйте sorted()
original = [3, 1, 4, 1, 5]
sorted_list = sorted(original)
print(f"Оригинал: {original}")
# Оригинал: [3, 1, 4, 1, 5]
print(f"Отсортированная копия: {sorted_list}")
# Отсортированная копия: [1, 1, 3, 4, 5]
```

##### Saraksta kopēšana

```python
# Создаем список
original = [1, 2, 3]

# Присваивание не создает копию — обе переменные указывают на один список
reference = original
reference.append(4)
print(f"Оригинал после изменения ссылки: {original}")
# Оригинал после изменения ссылки: [1, 2, 3, 4]

# Правильные способы копирования списка:
# 1. Метод copy()
copy1 = original.copy()

# 2. Использование среза [:]
copy2 = original[:]

# 3. Функция list()
copy3 = list(original)

# Проверим, что копии не связаны с оригиналом
copy1.append(5)
print(f"Оригинал: {original}")
# Оригинал: [1, 2, 3, 4]
print(f"Копия 1: {copy1}")
# Копия 1: [1, 2, 3, 4, 5]
```

#### Praktiskais piemērs

```python
# Список студентов и их оценок
students = ["Анна", "Иван", "Мария", "Петр", "Елена"]
grades = [95, 82, 90, 78, 88]

# Нахождение студента с наивысшим баллом
highest_score = max(grades)
top_student_index = grades.index(highest_score)
print(f"Лучший студент: {students[top_student_index]} с оценкой {highest_score}")
```

```python
numbers = list(map(int, input().split()))

# Добавьте число 100 в конец списка
numbers.append(100)

# Удалите первый элемент из списка
del numbers[0]

# Выведите измененный список в одну строку, с элементами, разделенными пробелами
print(*numbers)
```

---
### ⇄ Saistības
Avots >>> [Списки — Интерактивный курс по Python](https://python-academy.org/ru/guide/lists)
Iepriekšēja lapa >>> [[Operatori if, elif, else...]]
Nākama lapa >>> [[Korteži]]
___