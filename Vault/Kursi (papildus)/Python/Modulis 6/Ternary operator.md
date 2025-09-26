___

**Datums:** 2025-07-30   
**Laiks:** 15:24 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Ternary operator

`Ternary operator` Python valodā ļauj veikt nosacījuma pārbaudes un piešķirt vērtības vai veikt darbības vienā rindā. To sauc arī par nosacījuma izteiksmi, jo tā novērtē nosacījumu un atgriež vienu vērtību, ja nosacījums ir `True`, un citu, ja tas ir `False`.

Papildus var veikt arī iterācijas `for` ciklā:

```python
ipatnis = ['-suns', 'kakis', '-Aligators']
normals = [vards[1:] if vards.startswith('-') else vards for vards in ipatnis]
```
##### Parastais piems

```python
n = 5
res = "Even" if n % 2 == 0 else "Odd"
print(res) # Odd
```

##### Piemērs izmantojot vairākus `if` operatorus

```
Syntax: value_if_true if condition else value_if_false
```

```python
n = -5

res = "Positive" if n > 0 else "Negative" if n < 0 else "Zero"
print(res) # Negative


# analogisks pieraksts
if n > 0:
    res = "Positive"
else:
    if n < 0:
        res = "Negative"
    else:
        res = "Zero"
```

##### Piemērs izmantojot `tuple`

```
Syntax: (condition_is_false, condition_is_true)[condition]
```

```python
n = 7
res = ("Odd", "Even")[n % 2 == 0]
print(res) # Odd
```

##### Piemērs izmantojot `dictionary`

```
Syntax: lambda x: value_if_true if condition else value_if_false
```

```python
a = 10
b = 20
max = (lambda x, y: x if x > y else y)(a, b)
print(max) # 20
```

##### Piemērs ar `print` funkciju

```
Syntax: print(value_if_true if condition else value_if_false)
```

```python
a = 10
b = 20

print("a is greater" if a > b else "b is greater")
# b is greater
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[pass operators]]
Nākama lapa >>> [[Navigācija - Python strukturēts]]

---
### ⇄ Saistības

Avots >>> [Ternary Operator in Python - GeeksforGeeks](https://www.geeksforgeeks.org/python/ternary-operator-in-python/)
Iepriekšēja lapa >>> [[Modulis re]]
Nākama lapa >>> [[Navigācija - Python]]

___