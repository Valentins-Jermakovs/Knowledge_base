___

**Datums:** 2025-07-26   
**Laiks:** 12:44 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### `for` cikls

`for` cikls ļauj iterēt pa elementu sarakstam.

- `i` - iterators;
- `text` - iterējamais saraksts;
- `statement` - loģika, kas izpildās iterācijās;

```python
for i in text:
	statement
```

```python
text = 'Hello world!'

for i in text:
	print(i)

# H
# e
# l
# l
# o
# 
# w
# o
# r
# l
# d
# !
```

```python
text = 'Hello World'
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text:
	index = alphabet.find(char)
	print(char, index)
```

> [!NOTE] Svarīgi!
> `for` cikls atgriež elementu, nevis iteratoru. Iteratoru var iegūt `while` ciklā. Tā ir galvenā atšķirība no citām programmēšanas valodām.

##### Papildus informācija

Ja kodā netiek izmantots iterators no `for` cikla, tad to var apzīmēt kā `_` simbolu.

```python
for _ in range(length):
    password += secrets.choice(all_characters)
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Navigācija - Python strukturēts]]
Nākama lapa >>> [[Kursi (papildus)/Python/Modulis 3/while cikls|while cikls]]

---
### ⇄ Saistības

Avots >>> [freecodecamp.org/learn/scientific-computing-with-python/learn-string-manipulation-by-building-a-cipher/step-23](https://www.freecodecamp.org/learn/scientific-computing-with-python/learn-string-manipulation-by-building-a-cipher/step-23)
Iepriekšēja lapa >>> [[Konsoles izvada formatēšana]]
Nākama lapa >>> [[Kursi (papildus)/Python/Modulis 1/Salīdzināšanas operatori]]

___