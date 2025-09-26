___

**Datums:** 2025-07-03   
**Laiks:** 18:01 
❚ **Tagi:** #Python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Operators `if`

```python
# Простой пример оператора if
age = 18

if age >= 18:
    print("Вы совершеннолетний!")

print("Эта строка выполнится всегда, независимо от условия.")
# Вы совершеннолетний!
# Эта строка выполнится всегда, независимо от условия.
```

#### Operators `else`

```python
temperature = 15

if temperature > 20:
    print("Сегодня тепло, можно идти в футболке!")
else:
    print("Сегодня прохладно, возьмите куртку!")
# Сегодня прохладно, возьмите куртку!
```

#### Konstrukcija `elif`

```python
temperature = 25

if temperature < 0:
    print("Очень холодно! Наденьте тёплую куртку и шапку!")
elif temperature < 10:
    print("Холодно. Оденьтесь теплее.")
elif temperature < 20:
    print("Прохладно. Лёгкая куртка не помешает.")
elif temperature < 30:
    print("Тепло. Футболка и шорты подойдут.")
else:
    print("Жарко! Возьмите с собой воду!")
# Тепло. Футболка и шорты подойдут.
```

##### Ieliktas konstrukcijas

```python
age = 25
has_license = True

if age >= 18:
    print("Вы совершеннолетний.")

    if has_license:
        print("Вы можете водить автомобиль.")
    else:
        print("Для вождения автомобиля вам необходимо получить права.")
else:
    print("Вы несовершеннолетний и не можете водить автомобиль.")
# Вы совершеннолетний.
# Вы можете водить автомобиль.
```

```python
age = 25
has_license = True

if age >= 18 and has_license:
    print("Вы совершеннолетний и можете водить автомобиль.")
elif age >= 18 and not has_license:
    print("Вы совершеннолетний, но для вождения автомобиля вам необходимо получить права.")
else:
    print("Вы несовершеннолетний и не можете водить автомобиль.")
# Вы совершеннолетний и можете водить автомобиль.
```

##### Ternara operatori

```python
age = 20

# Обычная запись через if-else
if age >= 18:
    status = "совершеннолетний"
else:
    status = "несовершеннолетний"

print(f"Обычная запись: Вы {status}")
# Обычная запись: Вы совершеннолетний

# Та же логика, но с использованием тернарного оператора
status = "совершеннолетний" if age >= 18 else "несовершеннолетний"
print(f"Тернарный оператор: Вы {status}")
# Тернарный оператор: Вы совершеннолетний
```

Ternara operatora sintakse:

```python
значение_если_истина if условие else значение_если_ложь
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Kursi (papildus)/Python/Modulis 1/Salīdzināšanas operatori]]
Nākama lapa >>> [[not operators]]

---
### ⇄ Saistības

Avots >>> [Условная конструкция. Оператор if — Интерактивный курс по Python](https://python-academy.org/ru/guide/if-statement)
Iepriekšēja lapa >>> [[Kursi (papildus)/Python/Academy/Funkcijas]]
Nākama lapa >>> [[Kursi (papildus)/Python/Academy/Saraksti]]

___