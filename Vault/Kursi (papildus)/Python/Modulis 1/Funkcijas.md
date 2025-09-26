___
**Datums:** 2025-07-26   
**Laiks:** 15:21 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Funkcijas

> [!NOTE] Funkcija
> Koda bloks, kas veic kādu konkrētu uzdevumu un var tikt izmantots vairākas reizes.

```python
def function_name():
    <code>
```

Piemērs ar šifru:

```python
text = 'Hello Zaira'
shift = 3

def caesar():
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in text.lower():
        if char == ' ':
            encrypted_text += char
        else:
            index = alphabet.find(char)
            new_index = (index + shift) % len(alphabet)
            encrypted_text += alphabet[new_index]
    print('plain text:', text)
    print('encrypted text:', encrypted_text)
```

>Mainīgajiem, kas definēti ārpus funkcijas, ir globāla darbības joma, un tiem var piekļūt no jebkuras jūsu koda daļas.

>Mainīgie, kas definēti funkcijā, ir lokāli šai funkcijai un tiem nevar piekļūt ārpus tās.

Lai izsaukt funkciju, uzraksti tās nosaukumu un `()`, ja nepieciešams, nodod parametrus.

```python
function_name()
```

Funkcija ar parametriem:

```python
def function_name(param_1, param_2):
    <code>
```

##### `return`

`return` ļauj atgriezt datus, rezultatu no funkcijas darbības.

```python
def foo():
    return 'spam'
```

##### Noklusējuma vērtības

Funkciju parametri var būt definēti arī iepriekš ar noklusējuma vērtībām:

```python
def foo(a, b, c=value):
    <code>
```

---
### ⇄ Saistības
Avots >>> [freecodecamp.org/learn/scientific-computing-with-python/learn-string-manipulation-by-building-a-cipher/step-49](https://www.freecodecamp.org/learn/scientific-computing-with-python/learn-string-manipulation-by-building-a-cipher/step-49)
Iepriekšēja lapa >>> [[elif nosacījums]]
Nākama lapa >>> [[isalpha() metode]]
___