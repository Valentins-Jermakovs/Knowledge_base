___
**Datums:** 2025-07-04   
**Laiks:** 12:56 
❚ **Tagi:** #Python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Kas ir iterācija?

> [!NOTE] Iterācija
> Iterācija ir viena instrukciju kopas izpilde. Cikls ir konstrukcija, kas ļauj koda bloku izpildīt atkārtoti, ja vien ir izpildīts noteikts nosacījums.

#### Cikls `for`

```python
# Простой пример цикла for
fruits = ["яблоко", "банан", "вишня"]

for fruit in fruits:
    print(f"Я люблю {fruit}!")
# Я люблю яблоко!
# Я люблю банан!
# Я люблю вишня!
```

```python
# Использование range() для создания последовательности чисел
for i in range(5):
    print(f"Число: {i}")
# Число: 0
# Число: 1
# Число: 2
# Число: 3
# Число: 4
```

```python
# Варианты использования range()

# range(stop): от 0 до stop-1
for i in range(3):
    print(i, end=" ")
print()
# 0 1 2

# range(start, stop): от start до stop-1
for i in range(2, 5):
    print(i, end=" ")
print()
# 2 3 4

# range(start, stop, step): от start до stop-1 с шагом step
for i in range(1, 10, 2):  # Нечетные числа от 1 до 9
    print(i, end=" ")
# 1 3 5 7 9
```

```python
# Перебор символов в строке
message = "Python"

for char in message:
    print(char)
# P
# y
# t
# h
# o
# n
```

```python
# Получение индексов и значений
fruits = ["яблоко", "банан", "вишня"]

for index, fruit in enumerate(fruits):
    print(f"Индекс {index}: {fruit}")
# Индекс 0: яблоко
# Индекс 1: банан
# Индекс 2: вишня
```

#### Cikls `while`

```python
count = 1

while count <= 5:
    print(f"Цикл выполняется в {count}-й раз")
    count += 1
# Цикл выполняется в 1-й раз
# Цикл выполняется в 2-й раз
# Цикл выполняется в 3-й раз
# Цикл выполняется в 4-й раз
# Цикл выполняется в 5-й раз
```

#### Ciklu pārvaldība
`break` - iziet no cikla
`continue` - sākt jauno iterāciju, izlaist esošo.

> Pēc cikla var ielikt `else` bloku, kas izpildīsies, ja cikls veiksmīgi pabeidza savu darbību.

```python
# Использование else с циклом
for i in range(5):
    print(i, end=" ")
else:
    print("\nЦикл завершен нормально")
# 0 1 2 3 4
# Цикл завершен нормально

# Пример с break - блок else не выполнится
for i in range(5):
    print(i, end=" ")
    if i == 2:
        break
else:
    print("\nЭта строка не будет выведена, так как цикл прерван")
# 0 1 2
```

---
### ⇄ Saistības
Avots >>> [Итерации и циклы — Интерактивный курс по Python](https://python-academy.org/ru/guide/loops)
Iepriekšēja lapa >>> [[Kursi (papildus)/Python/Academy/Vārdnīcas]]
Nākama lapa >>> [[Navigācija - Python]]
___