___

**Datums:** 2025-07-03   
**Laiks:** 17:44 
❚ **Tagi:** #Python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Kas ir funkcija?

> [!NOTE] Funkcija
> Funkcija ir nosaukts koda bloks, kas veic noteiktu uzdevumu un ko var izsaukt no citām programmas daļām vairākas reizes.

#### Funkcijas izveide un izsaukšana

```python
# Простой пример функции
def greet():
    print("Привет, мир!")

# Вызов функции
greet()
```

#### Funkcija ar parametriem

```python
# Функция с параметрами
def greet(name):
    print(f"Привет, {name}!")

# Вызов функции с аргументом
greet("Анна")
# Привет, Анна!
greet("Петр")
# Привет, Петр!
```

#### Atgriežamas vērtības

```python
# Функция с возвращаемым значением
def add(a, b):
    return a + b

# Использование результата функции
result = add(5, 3)
print(f"5 + 3 = {result}")
# 5 + 3 = 8
```

#### Funkciju parametri

##### Parametru nodošana

Pastāv 2 veidi kā nodot parametrus:

```python
# Функция с несколькими параметрами
def describe_pet(animal_type, pet_name):
    print(f"У меня есть {animal_type} по имени {pet_name}.")

# Позиционные аргументы
describe_pet("собака", "Шарик")

# Именованные аргументы
describe_pet(pet_name="Мурка", animal_type="кошка")
```

##### Parametri pēc noklusējuma

Var uzdot parametrus pēc noklusējuma:

```python
# Функция с параметрами по умолчанию
def describe_pet(pet_name, animal_type="собака"):
    print(f"У меня есть {animal_type} по имени {pet_name}.")

# Использование значения по умолчанию
describe_pet("Шарик")
# У меня есть собака по имени Шарик.
# Переопределение значения по умолчанию
describe_pet("Мурка", "кошка")
# У меня есть кошка по имени Мурка.
```

##### Nenoteikts parametru daudzums

```python
# Функция с произвольным количеством позиционных аргументов
def make_pizza(*toppings):
    print("Готовим пиццу со следующими начинками:")
    for topping in toppings:
        print(f"- {topping}")

make_pizza("пепперони")
# Готовим пиццу со следующими начинками:
#  - пепперони

make_pizza("грибы", "зеленый перец", "дополнительный сыр")
# Готовим пиццу со следующими начинками:
# - грибы
# - зеленый перец
# - дополнительный сыр

# Функция с произвольным количеством именованных аргументов
def build_profile(first, last, **user_info):
    profile = {}
    profile['first_name'] = first
    profile['last_name'] = last
    for key, value in user_info.items():
        profile[key] = value
    return profile

user_profile = build_profile('Анна', 'Иванова',
                           location='Москва',
                           field='программирование')
print(user_profile)
# {'first_name': 'Анна', 'last_name': 'Иванова', 'location': 'Москва', 'field': 'программирование'}
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Navigācija - Python strukturēts]]
Nākama lapa >>> [[Lambda funkcijas]]

---
### ⇄ Saistības

Avots >>> [Функции — Интерактивный курс по Python](https://python-academy.org/ru/guide/functions)
Iepriekšēja lapa >>> [[Loģiskais datu tips]]
Nākama lapa >>> [[Operatori if, elif, else...]]

___