___

**Datums:** 2025-07-30   
**Laiks:** 13:27 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Modulis

Modulis `re` tiek izmantos darbam ar `regex` (regular expressions). `regex` izmanto paroļu, epastu, telefona numuru utt. validācijai.

Modulis `re` satur metodes, lai meklēt sakritību ar `regex` un mainīgo/teksta virkni.

```python
import re

# šis bloks strādā bez re
constraints = [
    (nums, r'\d'),
    (special_chars, fr'[{symbols}]'),
    (uppercase, r'[A-Z]'),
    (lowercase, r'[a-z]')
]

# šeit notiek sakritību meklēšana, vajadzīgs re modulis
# Check constraints        
    if all(
        constraint <= len(re.findall(pattern, password)) for constraint, pattern in constraints
    ):
        break
```

| Metodes        | Ko dara?                                                                          |
| -------------- | --------------------------------------------------------------------------------- |
| `re.search()`  | Meklē pirmo sakritību                                                             |
| `re.findall()` | Atrod visas sakritības                                                            |
| `re.sub()`     | Aizvieto fragmentu                                                                |
| `re.split()`   | Sadala pēc sakritības ar šablonu un atgriež sarakstu ar `string` tipa elementiem. |
#### Piemēri

##### Medote `re.search()`

Ja sakritību atrod, atgriež objektu `Match`, pretēji `None`

```python
import re
 
text = "Python is an amazing programming language."
pattern = "amazing"
 
match = re.search(pattern, text)
if match:
    print("Совпадение найдено:", match.group())
else:
    print("Совпадение не найдено")
# Совпадение найдено: amazing
```

##### Metode `re.findall()`

Metode atgriež sarakstu.

```python
import re
 
text = "Python is an amazing programming language. Python is widely used."
pattern = "Python"
 
matches = re.findall(pattern, text)
print("Совпадений найдено:", len(matches))

# Совпадений найдено: 2
```

##### Metode `re.sub()`

```python
import re
 
text = "Python is an amazing programming language."
pattern = "amazing"
replacement = "awesome"
 
result = re.sub(pattern, replacement, text)
print("Результат замены:", result)

# Результат замены: Python is an awesome programming language.
```

##### Metode `re.split()`

```python
import re
 
text = "Python is an amazing programming language."
pattern = r"\s+"  # шаблон для разделения по пробелам
 
words = re.split(pattern, text)
print("Список слов:", words)

# Список слов: ['Python', 'is', 'an', 'amazing', 'programming', 'language.']
```

#### Pamata elementi `regex`

- `.` – любой символ, кроме перевода строки;
- `^` – начало строки;
- `$` – конец строки;
- `*` – ноль или более повторений предыдущего символа;
- `+` – одно или более повторений предыдущего символа;
- `?` – ноль или одно повторение предыдущего символа;
- `{m,n}` – от `m` до `n` повторений предыдущего символа;
- `[...]` – набор символов;
- `[^...]` – исключающий набор символов;
- `\` – экранирование специальных символов;
- `|` – альтернатива (или);
- `(...)` – группировка.

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Modulis secrets]]
Nākama lapa >>> [[Sevis veidota moduļa (faila) imports]]

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Modulis string]]
Nākama lapa >>> [[Ternary operator]]

___