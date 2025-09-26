___

**Datums:** 2025-07-03   
**Laiks:** 11:00 

❚ **Tagi:** #Python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Mainīgie

> [!NOTE] Mainīgais
> Mainīgais Python valodā ir nosaukta atsauce uz objektu atmiņā, kura tips tiek noteikts dinamiski un var mainīties.

Python valodā darbs ar mainīgajiem ir ārkārtīgi vienkāršs:

- Nav jānorāda tips — Python to noteiks jūsu vietā.
- Mainīgā tipu var mainīt jebkurā laikā.

#### Mainīgo izveidošana

```python
# Создание переменных различных типов
name = "Иван"          # Строковая переменная
age = 25               # Целочисленная переменная
height = 1.85          # Переменная с плавающей точкой
is_student = True      # Логическая переменная
courses = ["Python", "SQL", "JavaScript"]  # Переменная-список
```

#### Funkcija `print()`

Šī funkcija ļauj izvadīt tekstu, datus konsolē.

```python
name = "Иван"
# Используем переменную в строке с приветствием
print("Привет, " + name + "! 👋")

age = 25
# Используем переменную в вычислении
next_year_age = age + 1
print(f"В следующем году тебе будет {next_year_age} лет! 🎂")
```

#### Vairāku mainīgo definēšana vienlaikus

```python
# Присваиваем одно значение нескольким переменным
x = y = z = 0
print(f"x = {x}, y = {y}, z = {z}")

# Присваиваем разные значения нескольким переменным
a, b, c = 1, 2, 3
print(f"a = {a}, b = {b}, c = {c}")
```

#### Funkcija `type()`

Šī funkcija ļauj uzzināt mainīgā datu tipu.

```python
name = "Иван"
age = 25
height = 1.85
is_student = True

# Определение типов переменных
print(f"{name}: {type(name)}")

print(f"{age}: {type(age)}")

print(f"{height}: {type(height)}")

print(f"{is_student}: {type(is_student)}")
```

#### Mainīgo definēšanas labā prakse

Zemāk ir piemērs, kā definēt mainīgos.

```python
# Допустимые имена
name = "Иван"
age_in_years = 25
_private_variable = "Непубличная информация"

# Недопустимые имена
# 2name = "Нельзя начинать с цифры"
# my-name = "Нельзя использовать дефис"
# class = "Зарезервированное слово"
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Kursi (papildus)/Python/Modulis 1/Mainīgo definēšana]]
Nākama lapa >>> [[Globālie un lokālie mainīgie]]

---
### ⇄ Saistības

Avots >>> [Переменные — Интерактивный курс по Python](https://python-academy.org/ru/guide/variables)
Iepriekšēja lapa >>> [[Navigācija - Python]]
Nākama lapa >>> [[Globālie un lokālie mainīgie]]

___