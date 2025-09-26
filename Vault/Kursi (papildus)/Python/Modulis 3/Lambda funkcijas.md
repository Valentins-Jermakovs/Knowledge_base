___

**Datums:** 2025-07-27   
**Laiks:** 16:31 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Lambda funkcijas

Tas ir vienkāršas, anonīmas funkcijas, kas paredzētas ļoti vienkāršam uzdevumam.

```python
lambda x: expr
```

Kur:
- `lambda` - atslēgvārds, tas ir obligāts;
- `x` - parametrs;
- `expr` - kas notiek ar parametru jeb `expression`.

```python
test = lambda x: x * 2
print(test(3)) # Output: 6
```

##### `map()` metode

Metode `map()` ļauj nodot lambda funkcijai vairākus parametrus, sarakstu.

```python
test = lambda x: x * 2
print(list(map(test, [2, 3, 5, 8])))

# [4, 6, 10, 16]
```

Šeit obligāti nepieciešams izmantot `list()` funkciju, kas `map()` pārveido sarakstā, lai izvadītu rezultātu konsolē.

`sum()` funkcija ļauj uzzināt visu elementu summu.

```python
test = lambda x: x * 2
print(sum(map(test, [2,3,5,8])))  # 36
```

##### `filter()` metode

Kā pirmo parametru, pieņem funkciju, kā otro parametru, pieņem sarakstu, pa kuru iterē.

```python
def filter_expenses_by_category(expenses, category):
    filter(lambda expense: expense['category'] == category, expenses)
```

Šeit atgriež iteratorus, kuriem `True`, pēc funkcijas izpildes.

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Kursi (papildus)/Python/Academy/Funkcijas|Funkcijas]]
Nākama lapa >>> [[main funkcija]]

---
### ⇄ Saistības

Avots >>> [Learn Lambda Functions by Building an Expense Tracker: Step 19 \| freeCodeCamp.org](https://www.freecodecamp.org/learn/scientific-computing-with-python/learn-lambda-functions-by-building-an-expense-tracker/step-19)
Iepriekšēja lapa >>> [[Kursi (papildus)/Python/Modulis 3/Vārdnīcas]]
Nākama lapa >>> [[Lambda funkcijas]]

___