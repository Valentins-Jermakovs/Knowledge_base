___

**Datums:** 2025-07-04   
**Laiks:** 11:25 
❚ **Tagi:** #Python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Kas ir vārdnīca?

> [!NOTE] Vārdnīca
> Vārdnīca Python valodā ir atslēgu-vērtību pāru kolekcija. Vārdnīcu var uzskatīt par tālruņu grāmatu, kur cilvēku vārdi (atslēgas) ir saistīti ar viņu tālruņu numuriem (vērtībām).

#### Vārdnīcas izveide

##### Vārdnīcas veidošana ar `{}`

```python
# Пустой словарь
empty_dict = {}

# Словарь с данными
person = {"name": "John", "age": 30, "city": "New York"}
print(person)
# {'name': 'John', 'age': 30, 'city': 'New York'}

# Вложенные словари
nested = {
    "person": {"name": "Mary", "age": 25},
    "contacts": {"email": "mary@example.com", "phone": "+1234567890"}
}
print(nested["person"])
# {'name': 'Mary', 'age': 25}
```

##### Ar konstruktoru `dict()`

```python
# Пустой словарь
empty_dict = dict()

# Из списка кортежей (пар ключ-значение)
pairs = [("name", "Anna"), ("age", 28), ("city", "Berlin")]
person = dict(pairs)
print(person)
# {'name': 'Anna', 'age': 28, 'city': 'Berlin'}

# С использованием именованных аргументов (только для строковых ключей)
settings = dict(theme="dark", font_size=12, notifications=True)
print(settings)
# {'theme': 'dark', 'font_size': 12, 'notifications': True}
```

##### Ar ģeneratoru

```python
# Словарь квадратов чисел (число: квадрат числа)
squares = {x: x**2 for x in range(1, 6)}
print(squares)
# {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

##### Ar metodi `fromkeys`

```python
# Создание словаря с заданными ключами и одинаковым значением для всех
keys = ["name", "age", "city"]
defaults = dict.fromkeys(keys, None)
print(defaults)
# {'name': None, 'age': None, 'city': None}
```

#### Pieeja pie vārdnīcas elementiem

##### Pieeja pēc atslēgas

```python
person = {"name": "John", "age": 30, "city": "New York"}

# Получение значения по ключу
name = person["name"]
print(name)
# John

# Безопасный способ с помощью метода get()
phone = person.get("phone")  # Вернет None, если ключа нет
print(phone)
# None

# Метод get() с значением по умолчанию
phone = person.get("phone", "Not specified")
print(phone)
# Not specified
```

##### Pārbaude uz atslēgas esamību

```python
person = {"name": "John", "age": 30, "city": "New York"}

# Проверка наличия ключа
print("name" in person)
# True

print("phone" not in person)
# False
```

##### Pieeja pie ieliktām vārdnīcām

```python
nested = {
    "person": {"name": "Mary", "age": 25},
    "contacts": {"email": "mary@example.com", "phone": "+1234567890"}
}

# Доступ к значениям во вложенных словарях
name = nested["person"]["name"]
print(name)
# Mary

# Безопасный доступ с помощью get()
email = nested.get("contacts", {}).get("email")
print(email)
# mary@example.com

# Если путь не существует, вернется None или значение по умолчанию
website = nested.get("contacts", {}).get("website", "Not specified")
print(website)
# Not specified
```

#### Vārdnīcas modificēšana

##### Elementu pievienošana, modificēšana

```python
# Создаем словарь
person = {"name": "John", "age": 30}

# Добавление нового ключа и значения
person["city"] = "New York"
print(person)
# {'name': 'John', 'age': 30, 'city': 'New York'}

# Изменение значения существующего ключа
person["age"] = 31
print(person)
# {'name': 'John', 'age': 31, 'city': 'New York'}

# Использование метода update() для массового обновления
person.update({"age": 32, "job": "developer", "language": "Python"})
print(person)
# {'name': 'John', 'age': 32, 'city': 'New York', 'job': 'developer', 'language': 'Python'}
```

##### Elementu dzēšana

```python
person = {"name": "John", "age": 30, "city": "New York", "job": "developer"}

# Удаление элемента по ключу с помощью del
del person["job"]
print(person)
# {'name': 'John', 'age': 30, 'city': 'New York'}

# Удаление и возврат элемента с помощью pop()
age = person.pop("age")
print(age)
# 30
print(person)
# {'name': 'John', 'city': 'New York'}

# pop() с значением по умолчанию (не вызывает ошибку, если ключа нет)
job = person.pop("job", "Not specified")
print(job)
# Not specified

# Удаление и возврат произвольного элемента с помощью popitem()
# В Python 3.7+ возвращает последний добавленный элемент
item = person.popitem()
print(item)
# ('city', 'New York')
print(person)
# {'name': 'John'}

# Удаление всех элементов
person.clear()
print(person)
# {}
```

#### Vārdnīcu metodes

##### Atslēgu, vērtību un atslēgu-vērtību pāru iegūšana

```python
person = {"name": "John", "age": 30, "city": "New York"}

# Получение всех ключей
keys = person.keys()
print(keys)
# dict_keys(['name', 'age', 'city'])

# Получение всех значений
values = person.values()
print(values)
# dict_values(['John', 30, 'New York'])

# Получение всех пар ключ-значение
items = person.items()
print(items)
# dict_items([('name', 'John'), ('age', 30), ('city', 'New York')])

# Объекты dict_keys, dict_values и dict_items являются представлениями словаря
# Они динамически отражают изменения в словаре
person["job"] = "developer"
print(keys)
# dict_keys(['name', 'age', 'city', 'job'])

# Преобразование представлений в списки
keys_list = list(keys)
print(keys_list)
# ['name', 'age', 'city', 'job']
```

##### Vārdnīcu kopēšana

```python
import copy

# Словарь с вложенной структурой
original = {"name": "John", "settings": {"theme": "dark"}}

# Поверхностная и глубокая копии
shallow_copy = original.copy()
deep_copy = copy.deepcopy(original)

# Изменение простого ключа работает одинаково в обоих случаях
shallow_copy["name"] = "Peter"
deep_copy["name"] = "Alice"
print(f"original['name']: {original['name']}")  # Остается John
# original['name']: John

# Различия проявляются при изменении вложенных структур
shallow_copy["settings"]["theme"] = "light"
print(f"После shallow copy - original['settings']['theme']: {original['settings']['theme']}")  # Меняется!
# После shallow copy - original['settings']['theme']: light

# Создадим новый оригинал для демонстрации deep copy
original = {"name": "John", "settings": {"theme": "dark"}}
deep_copy = copy.deepcopy(original)
deep_copy["settings"]["theme"] = "light"
print(f"После deep copy - original['settings']['theme']: {original['settings']['theme']}")  # Не меняется
# После deep copy - original['settings']['theme']: dark
```

##### Vārdnīcu apvienošana

```python
# Объединение словарей с update
dict1 = {"a": 1, "b": 2}
dict2 = {"b": 3, "c": 4}

# Создаем копию dict1 и обновляем её данными из dict2
merged = dict1.copy()
merged.update(dict2)
print(merged)
# {'a': 1, 'b': 3, 'c': 4}

# В Python 3.9+ можно использовать оператор |
# merged = dict1 | dict2
```

##### Noklusējuma vērtību iestatīšana

```python
# Подсчет частоты слов
counts = {}
text = "one two one two three"
words = text.split()

# Способ 1: проверка наличия ключа
for word in words:
    if word in counts:
        counts[word] += 1
    else:
        counts[word] = 1
print(counts)
# {'one': 2, 'two': 2, 'three': 1}

# Способ 2: использование get()
counts = {}
for word in words:
    counts[word] = counts.get(word, 0) + 1
print(counts)
# {'one': 2, 'two': 2, 'three': 1}
```

#### Iterācija pa vārdnīcām

```python
person = {"name": "John", "age": 30, "city": "New York"}

# Итерация по ключам (способ по умолчанию)
print("Итерация по ключам:")
for key in person:
    print(key, ":", person[key])
# Итерация по ключам:
# name : John
# age : 30
# city : New York

# Итерация по значениям
print("Итерация по значениям:")
for value in person.values():
    print(value)
# Итерация по значениям:
# John
# 30
# New York

# Итерация по парам ключ-значение
print("Итерация по парам ключ-значение:")
for key, value in person.items():
    print(key, ":", value)
# Итерация по парам ключ-значение:
# name : John
# age : 30
# city : New York
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Kopas]]
Nākama lapa >>> [[Navigācija - Python strukturēts]]

---
### ⇄ Saistības
Avots >>> [Словари — Интерактивный курс по Python](https://python-academy.org/ru/guide/dictionaries)
Iepriekšēja lapa >>> [[Kopas]]
Nākama lapa >>> [[Navigācija - Python]]

___