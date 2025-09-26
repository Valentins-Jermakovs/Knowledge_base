___
**Datums:** 2025-07-28   
**Laiks:** 11:22 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Programma

```python
def convert_to_snake_case(pascal_or_camel_cased_string):

    snake_cased_char_list = [
        '_' + char.lower() if char.isupper()
        else char
        for char in pascal_or_camel_cased_string
    ]

    return ''.join(snake_cased_char_list).strip('_')
```

---
### ⇄ Saistības
Avots >>> [Learn Python List Comprehension by Building a Case Converter Program: Step 23 \| freeCodeCamp.org](https://www.freecodecamp.org/learn/scientific-computing-with-python/learn-list-comprehension-by-building-a-case-converter-program/step-23)
Iepriekšēja lapa >>> [[Saraksta izveide no for cikla]]
Nākama lapa >>> [[Navigācija - Python]]
___