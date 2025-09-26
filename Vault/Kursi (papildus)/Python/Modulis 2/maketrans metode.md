___
**Datums:** 2025-07-27   
**Laiks:** 11:55 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### `str.maketrans`

Šī metode ļauj izveidot tulkojuma tabulu. Šāda tabula tiek izmantota, lai aizvietot norādītos simbolus ar kādiem citiem simboliem.

```python
str.maketrans({'t': 'c', 'l': 'b'})
```

Piemēram, šeit visi `t` tiks aizvietoti ar `c` un visi `l` ar `b`.

```python
def main():
    card_number = '4111-1111-4555-1142'
    card_translation = str.maketrans({'-': '', ' ': ''})
    translated_card_number = card_number.translate(card_translation)
    print(translated_card_number)
main()

# 4111111145551142
```

Lai veiktu simbolu aizvietošanu, izmanto `.translate` metodi.

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[strip() metode]]
Nākama lapa >>> [[split() metode]]

---
### ⇄ Saistības

Avots >>> [Learn How to Work with Numbers and Strings by Implementing the Luhn Algorithm: Step 3 \| freeCodeCamp.org](https://www.freecodecamp.org/learn/scientific-computing-with-python/learn-how-to-work-with-numbers-and-strings-by-implementing-the-luhn-algorithm/step-3)
Iepriekšēja lapa >>> [[main funkcija]]
Nākama lapa >>> [[string konvertācija uz int]]

___