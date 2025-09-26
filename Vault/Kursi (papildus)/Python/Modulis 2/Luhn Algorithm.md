___
**Datums:** 2025-07-27   
**Laiks:** 12:52 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Algoritms

Šis algoritms tiek izmantots bankas karšu numuru, telefonu IMEI validācijai.
Ja summa ir 10, rezultāts tiek uzskatīts par validētu/pieņemtu.

```python
def verify_card_number(card_number):
    sum_of_odd_digits = 0
    card_number_reversed = card_number[::-1]
    odd_digits = card_number_reversed[::2]

    for digit in odd_digits:
        sum_of_odd_digits += int(digit)

    sum_of_even_digits = 0
    even_digits = card_number_reversed[1::2]
    for digit in even_digits:
        number = int(digit) * 2
        if number >= 10:
            number = (number // 10) + (number % 10)
        sum_of_even_digits += number
    total = sum_of_odd_digits + sum_of_even_digits
    return total % 10 == 0

def main():
    card_number = '4111-1111-4555-111'
    card_translation = str.maketrans({'-': '', ' ': ''})
    translated_card_number = card_number.translate(card_translation)

    if verify_card_number(translated_card_number):
        print('VALID!')
    else:
        print('INVALID!')

main()
```

---
### ⇄ Saistības
Avots >>> [freecodecamp.org/learn/scientific-computing-with-python/learn-how-to-work-with-numbers-and-strings-by-implementing-the-luhn-algorithm/step-35](https://www.freecodecamp.org/learn/scientific-computing-with-python/learn-how-to-work-with-numbers-and-strings-by-implementing-the-luhn-algorithm/step-35)
Iepriekšēja lapa >>> [[string konvertācija uz int]]
Nākama lapa >>> [[Navigācija - Python]]
___