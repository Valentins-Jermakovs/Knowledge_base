___

**Datums:** 2025-07-03   
**Laiks:** 12:07 
❚ **Tagi:** #Python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Teksta definēšana

```python
# Строки в одинарных кавычках
single_quotes = 'Привет, мир!'
print(single_quotes)

# Строки в двойных кавычках
double_quotes = "Python - это здорово!"
print(double_quotes)

# Многострочные строки в тройных кавычках
multi_line = """Это многострочная строка.
Она может занимать несколько строк
и сохраняет все переносы строк."""
print(multi_line)
```

#### Simbolu ekranēšana

```python
# Использование кавычек внутри строк с экранированием
quote_inside = "Он сказал: \"Привет!\""
print(quote_inside)

path = "C:\\Program Files\\Python"
print(path)

# Часто используемые последовательности экранирования
newline = "Первая строка.\nВторая строка."  # \n - перенос строки
print(newline)

tab = "Имя:\tИван"  # \t - табуляция
print(tab)
```

Speciālie simboli:

- `\n` — izveido jaunu rindu
- `\t` — ​​​​pievieno tabulēšanas zīmi (atkāpi)
- `\\`— ļauj ievietot atpakaļvērsto slīpsvītru
- `\'` — pievieno vienu pēdiņu
- `\"` — pievieno dubultu pēdiņu

#### Operācijas ar teksta rindām

##### Teksta rindu apvienošana

```python
first_name = "Иван"
last_name = "Петров"
full_name = first_name + " " + last_name
print(full_name)

greeting = "Привет, " + full_name + "!"
print(greeting)
```

##### Teksta rindu atkārtošana

Var izvadīt simbolu konkrētas reizes:

```python
star_line = "*" * 10
print(star_line)

border = "=" * 20
print(border)

pattern = "+-" * 5
print(pattern)

# Можно создавать красивые заголовки
title = "МЕНЮ"
decorated_title = f"{border}\n{title.center(20)}\n{border}"
print(decorated_title)
```

##### Pieeja pie konkrētiem simboliem

Šeit tāda pati sistēma kā ar masīva elementiem.

```python
word = "Python"
first_letter = word[0]
second_letter = word[1]
last_letter = word[5]

print(f"Первая буква: {first_letter}")
print(f"Вторая буква: {second_letter}")
print(f"Последняя буква: {last_letter}")

# Можно также использовать отрицательные индексы для отсчета с конца
last_letter = word[-1]
second_last_letter = word[-2]
print(f"Последняя буква (с конца): {last_letter}")
print(f"Предпоследняя буква: {second_last_letter}")
```

##### Griezumi `slices`

No teksta rindas var izvilkt apakšrindu.

```python
message = "Python Programming"

# Синтаксис среза: строка[начало:конец:шаг]
# начало включается, конец исключается

first_word = message[0:6]     # первые 6 символов
print(f"Первое слово: {first_word}")
# Python
second_word = message[7:]      # от 7-го до конца
print(f"Второе слово: {second_word}")
# Programming
prefix = message[:6]           # от начала до 6-го (не включая 6-й)
print(f"Префикс: {prefix}")
# Python
every_second = message[::2]    # каждый второй символ
print(f"Каждая вторая буква: {every_second}")
# Pto rgamn
reversed_string = message[::-1]  # строка задом наперед
print(f"В обратном порядке: {reversed_string}")
# gnimmargorP nohtyP
```

##### Noderīgas metodes darbam ar teksta rindām

##### Teksta reģistra maiņa

```python
text = "Python Programming"

upper_case = text.upper()
print(f"Верхний регистр: {upper_case}")
# PYTHON PROGRAMMING
lower_case = text.lower()
print(f"Нижний регистр: {lower_case}")
# python programming
title_case = text.title()
print(f"Заглавные первые буквы: {title_case}")
# Python Programming
capitalized = "hello world".capitalize()
print(f"Только первая буква заглавная: {capitalized}")
# Hello world
```

##### Meklēšana tekstā un izmaiņu veikšana tajā

```python
text = "Python - это отличный язык программирования"

# Поиск подстроки
position = text.find("отличный")
print(f"Слово 'отличный' начинается с позиции: {position}")
# Слово 'отличный' начинается с позиции: 13
count = text.count("о")
print(f"Буква 'о' встречается {count} раза")
# Буква 'о' встречается 3 раза
# Проверка начала и конца строки
starts_with = text.startswith("Python")
print(f"Строка начинается с 'Python': {starts_with}")
# Строка начинается с 'Python': True
ends_with = text.endswith("!")
print(f"Строка заканчивается на '!': {ends_with}")
# Строка заканчивается на '!': False
# Проверка наличия подстроки
contains = "отличный" in text
print(f"Строка содержит слово 'отличный': {contains}")
# Строка содержит слово 'отличный': True
# Замена подстрок
new_text = text.replace("отличный", "прекрасный")
print(f"Текст после замены: {new_text}")
# Текст после замены: Python - это прекрасный язык программирования
```

##### Teksta rindu dalīšana un apvienošana

```python
# Разделение строки на список слов
sentence = "Python - это отличный язык программирования"
words = sentence.split()
print(f"Список слов: {words}")
# Список слов: ['Python', '-', 'это', 'отличный', 'язык', 'программирования']
# Разделение по конкретному разделителю
csv_data = "яблоко,банан,вишня"
fruits = csv_data.split(",")
print(f"Список фруктов: {fruits}")
# Список фруктов: ['яблоко', 'банан', 'вишня']
# Объединение списка в строку
words_to_join = ["Python", "это", "здорово"]
joined_sentence = " ".join(words_to_join)
print(f"Объединенное предложение: {joined_sentence}")
# Объединенное предложение: Python это здорово
# Объединение с другим разделителем
path_parts = ["C:", "Users", "Username", "Documents"]
path = "\\".join(path_parts)
print(f"Путь к файлу: {path}")
# Путь к файлу: C:\Users\Username\Documents
```

##### Lieko simbolu dzēšana

```python
text_with_spaces = "   Python   "
# Удаление пробелов с обоих концов
cleaned = text_with_spaces.strip()
print(f"Без пробелов: '{cleaned}'")
# Без пробелов: 'Python'
left_cleaned = text_with_spaces.lstrip()
print(f"Без пробелов слева: '{left_cleaned}'")
# Без пробелов слева: 'Python   '
right_cleaned = text_with_spaces.rstrip()
print(f"Без пробелов справа: '{right_cleaned}'")
# Без пробелов справа: '   Python'
# Удаление конкретных символов
text_with_dots = "...Python..."
without_dots = text_with_dots.strip('.')
print(f"Без точек: '{without_dots}'")
# Без точек: 'Python'
```

##### f-rindas

`f` rindas ļauj tekstā ievietot mainīgos.

```python
name = "Анна"
age = 25

# Просто добавьте 'f' перед строкой и вставляйте переменные в {}
greeting = f"Привет, меня зовут {name} и мне {age} лет."
print(greeting)
# Привет, меня зовут Анна и мне 25 лет.

# Можно вставлять выражения и форматировать вывод
price = 19.99
quantity = 3
total = f"Итого: {price * quantity:.2f} руб."
print(total)
# Итого: 59.97 руб.
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Skaitliskie tipi]]
Nākama lapa >>> [[Loģiskais datu tips]]

---
### ⇄ Saistības

Avots >>> [Строковые типы данных — Интерактивный курс по Python](https://python-academy.org/ru/guide/string-data-types)
Iepriekšēja lapa >>> [[Skaitliskie tipi]]
Nākama lapa >>> [[Loģiskais datu tips]]

___