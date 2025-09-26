___

**Datums:** 2025-07-28   
**Laiks:** 18:58 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Metode

Metode `split()` ļauj sadalīt `string` virkni elementos.

```python
string.split(separator, maxsplit) 
```

Kur:

- `separator` - simbols, no kura tiek atdalīts;
- `maxsplit` - nosaka, cik daudz sadalījumu veikt.

```python
txt = "welcome to the jungle"

x = txt.split()

print(x)

# ['welcome', 'to', 'the', 'jungle']
```

```python
txt = "hello, my name is Peter, I am 26 years old"

x = txt.split(", ")

print(x)

# ['hello', 'my name is Peter', 'I am 26 years old']
```

```python
txt = "apple#banana#cherry#orange"

# setting the maxsplit parameter to 1, will return a list with 2 elements!
x = txt.split("#", 1)

print(x)

# ['apple', 'banana#cherry#orange']
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[maketrans metode]]
Nākama lapa >>> [[isdigit() metode]]

---
### ⇄ Saistības

Avots >>> [Python String split() Method](https://www.w3schools.com/python/ref_string_split.asp)
Iepriekšēja lapa >>> [[Pamata matemātiskas operācijas]]
Nākama lapa >>> [[isdigit() metode]]

___