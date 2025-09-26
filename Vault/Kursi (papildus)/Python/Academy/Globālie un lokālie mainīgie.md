___
**Datums:** 2025-07-03   
**Laiks:** 11:22 
❚ **Tagi:** #Python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Globālie un lokālie mainīgie

![[ru_scope.webp]]

`Globālais mainīgais` - tāds mainīgais, kas atrodas ārpus funkcijas. To var izmantot visur.
`Lokālais mainīgais` - tāds mainīgais, kas tiek izmantots lokāli, vienas funkcijas ietvaros.

#### Globālais mainīgais

```python
# Создаем глобальную переменную
message = "Привет, мир!"

def show_message():
    # Используем глобальную переменную внутри функции
    print(message)

show_message()  # Вызываем функцию

print(f"Переменная вне функции: {message}")
```

#### Lokālie mainīgie

```python
def calculate_sum():
    # Локальные переменные
    a = 10
    b = 20
    result = a + b
    print(f"Сумма внутри функции: {result}")

calculate_sum()

# Попытка обратиться к локальной переменной вне функции
try:
    print(f"Пытаемся получить доступ к result: {result}")
except NameError as e:
    print(f"Ошибка: {e}")
```

#### Prioritāte lokāliem mainīgiem

Ja `globālam` un `lokālam` mainīgiem ir viens un tāds pats nosaukums, programma prioritātē ņems `lokālo.`

```python
x = "глобальная"

def test_scope():
    x = "локальная"  # Локальная переменная с тем же именем
    print(f"Внутри функции: x = {x}")

test_scope()

print(f"Вне функции: x = {x}")
```

#### Atslēgvārds `global`

Vārds `global` norāda programmai, funkcijai, kā tiks izmantots globālais mainīgais.

```python
x = "глобальная"

def modify_global():
    global x  # Указываем, что используем глобальную переменную
    x = "глобальная изменена"
    print(f"Внутри функции: x = {x}")

modify_global()

print(f"Вне функции: x = {x}")
```


---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Kursi (papildus)/Python/Academy/Mainīgie|Mainīgie]]
Nākama lapa >>> [[Kursi (papildus)/Python/Academy/Datu tipi]]

---
### ⇄ Saistības
Avots >>> [Область видимости переменных — Интерактивный курс по Python](https://python-academy.org/ru/guide/variable-scope)
Iepriekšēja lapa >>> [[Kursi (papildus)/Python/Academy/Mainīgie|Mainīgie]]
Nākama lapa >>> [[Kursi (papildus)/Python/Academy/Datu tipi]]

___