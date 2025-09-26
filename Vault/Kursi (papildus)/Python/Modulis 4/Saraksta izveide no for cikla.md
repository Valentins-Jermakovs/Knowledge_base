___

**Datums:** 2025-07-28   
**Laiks:** 11:09 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Saraksta izveide

Izņemot standarta `[]` variantu, var izmantot iekšējo `for` ciklu saraksta izveidei.

```python
snake_cased_char_list = ['_' + char.lower() for char in pascal_or_camel_cased_string]

# a_l_o_n_g_a_n_d_c_o_m_p_l_e_x_s_t_r_i_n_g
```

Papildus, šeit var ievietot arī `if` nosacījumu, un `for` cikls arbosies tikai tad, ja `if` atgriež `True`.

```python
snake_cased_char_list = ['_' + char.lower() for char in pascal_or_camel_cased_string if char.isupper()]
```

Arī `else` var tikt izmantots.

```python
snake_cased_char_list = ['_' + char.lower() if char.isupper() else char for char in pascal_or_camel_cased_string]
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Saraksta metodes]]
Nākama lapa >>> [[Saraksta ģenerators]]

---
### ⇄ Saistības

Avots >>> [Learn Python List Comprehension by Building a Case Converter Program: Step 19 \| freeCodeCamp.org](https://www.freecodecamp.org/learn/scientific-computing-with-python/learn-list-comprehension-by-building-a-case-converter-program/step-19)
Iepriekšēja lapa >>> [[strip() metode]]
Nākama lapa >>> [[convert_to_snake_case]]

___