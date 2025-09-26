___

**Datums:** 2025-07-26   
**Laiks:** 12:17 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### `.find()` metode

Šī metode ļauj uzzināt meklējama simbola pozīciju. Tā atgriež indeksu. Kā parametru tā pieņem simbolu vai indeksu.

```python
alphabet = 'abcdefghijklmnopqrstuvwxyz'
alphabet.find('z') # return the index of 'z'
```

Ja metode nespēj atrast meklējamo simbolu, tad tā atgriež `-1`

```python
text = 'Hello World'
alphabet = 'abcdefghijklmnopqrstuvwxyz'

print(alphabet.find(text[0]))
```

#### `.index()` metode

Dara to pašu, ko `.find()`, bet ja neatrod, atgriež `ValueError`.

```python
offset = alphabet.index(key_char)
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[string masīvs]]
Nākama lapa >>> [[isalpha() metode]]

---
### ⇄ Saistības

Avots >>> [freecodecamp.org/learn/scientific-computing-with-python/learn-string-manipulation-by-building-a-cipher/step-13](https://www.freecodecamp.org/learn/scientific-computing-with-python/learn-string-manipulation-by-building-a-cipher/step-13)
Iepriekšēja lapa >>> [[Metode type()]]
Nākama lapa >>> [[Konsoles izvada formatēšana]]

___