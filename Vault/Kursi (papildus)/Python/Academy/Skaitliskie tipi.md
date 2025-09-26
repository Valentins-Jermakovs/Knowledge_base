___

**Datums:** 2025-07-03   
**Laiks:** 11:31 
❚ **Tagi:** #Python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Skaitļi `int`

`int` - veseli skaitļi

```python
# Положительные и отрицательные целые числа
positive = 42
negative = -73
zero = 0

# Большие числа (в Python нет ограничения на размер целых чисел)
big_number = 1234567890123456789012345678901234567890

# Двоичные, восьмеричные и шестнадцатеричные числа
binary = 0b1010      # 10 в десятичной системе
octal = 0o756        # 494 в десятичной системе
hexadecimal = 0xFF   # 255 в десятичной системе

# Использование разделителя для удобства чтения больших чисел
million = 1_000_000  # Это то же самое, что и 1000000
```

#### Skaitļi `float`

`float` - skaitļi ar komatu

```python
# Числа с десятичной точкой
price = 19.99
pi_approx = 3.14159
negative_float = -0.5

# Экспоненциальная запись (научная нотация)
avogadro = 6.022e23  # 6.022 * 10^23
tiny = 1.6e-35      # 1.6 * 10^(-35)
```

#### Aritmētiskas operācijas 

Pamata operācijas ietver sevī:
- `+` saskaitīšanu
- `-` atņemšanu
- `*` reizināšanu
- `/` dalīšanu ar atlikumu
- `//` dalīšanu bez atlikuma
- `%` atlikums no dalīšanas
- `**` celšana pakāpē

```python
a = 10
b = 3

# Сложение
sum_result = a + b  # 13

# Вычитание
diff_result = a - b  # 7

# Умножение
mult_result = a * b  # 30

# Деление (всегда возвращает float)
div_result = a / b  # 3.3333333333333335

# Целочисленное деление (возвращает целую часть результата деления)
floor_div = a // b  # 3

# Остаток от деления
remainder = a % b  # 1

# Возведение в степень
power = a ** b  # 1000
```

#### Skaitļu noapaļošana

```python
# Округление до ближайшего целого
rounded = round(3.14159)  # 3

# Округление до указанного количества знаков после запятой
rounded_pi = round(3.14159, 2)  # 3.14

# Округление вниз (к меньшему целому)
import math
floor_value = math.floor(3.99)  # 3

# Округление вверх (к большему целому)
ceil_value = math.ceil(3.01)  # 4

# Отбрасывание дробной части
trunc_value = math.trunc(3.99)  # 3
```

#### Matemātiskas funkcijas

Modulis `math` ļauj izmantot daudzas noderīgas matemātiskas funkcijas, taču pirms to pielietošanas, nepieciešams `import math`:

```python
import math

# Константы
pi = math.pi      # 3.141592653589793
e = math.e        # 2.718281828459045

# Тригонометрические функции (аргументы в радианах)
sin_value = math.sin(math.pi / 2)  # 1.0
cos_value = math.cos(math.pi)      # -1.0
tan_value = math.tan(math.pi / 4)  # 1.0

# Обратные тригонометрические функции
asin_value = math.asin(1.0)  # 1.5707963267948966 (π/2)

# Логарифмы
log_value = math.log(10)      # натуральный логарифм, ln(10) = 2.302585092994046
log10_value = math.log10(100) # логарифм по основанию 10, log10(100) = 2.0

# Корни
sqrt_value = math.sqrt(16)    # квадратный корень, 4.0
```

#### Nejaušo skaitļu ģenerācija

Nejaušu skaitļu ģenerācijai izmanto moduli `random`. Pirms lietošanas `import random`:

```python
import random

# Случайное число от 0 до 1
random_float = random.random()  # например, 0.7593696548501615

# Случайное целое число в диапазоне
random_int = random.randint(1, 10)  # случайное целое от 1 до 10 включительно

# Случайное число с плавающей точкой в диапазоне
random_range = random.uniform(1.5, 3.5)  # например, 2.4378123553729193

# Случайный выбор из последовательности
random_choice = random.choice([1, 3, 5, 7, 9])  # случайный элемент из списка
```

#### Skaitļu metodes un funkcijas

`Python` valodā ir šādas iebūvētas metodes darbam ar skaitļiem.

```python
# Абсолютное значение
abs_value = abs(-10)  # 10

# Максимальное и минимальное значение
max_value = max(1, 5, 3, 9, 2)  # 9
min_value = min(1, 5, 3, 9, 2)  # 1

# Сумма последовательности
sum_value = sum([1, 2, 3, 4, 5])  # 15

# Преобразование других типов в числовые
int_from_str = int("42")     # 42
float_from_str = float("3.14")  # 3.14
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Kursi (papildus)/Python/Academy/Datu tipi]]
Nākama lapa >>> [[Teksta datu tips]]

---

### ⇄ Saistības
Avots >>> [Числовые типы данных — Интерактивный курс по Python](https://python-academy.org/ru/guide/numeric-data-types)
Iepriekšēja lapa >>> [[Kursi (papildus)/Python/Academy/Datu tipi]]
Nākama lapa >>> [[Teksta datu tips]]

___