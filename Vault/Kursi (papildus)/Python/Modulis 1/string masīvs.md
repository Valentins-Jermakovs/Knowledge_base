___

**Datums:** 2025-07-26   
**Laiks:** 11:56 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Par `string`

##### Indeksācija no pirmā līdz pēdējam simbolam

`string` ir elementu saraksts. Tas nozīmē, kā var manuāli piekļūt pie katra simbola, izmantojot indeksāciju.

```python
text = 'Hello World'
letter = text[6]

print(letter)  # W
print(text[6]) # W
```

<mark style="background: #FFB86CA6;">Indeksācija sākas no nulles!</mark>

##### Indeksācija no pēdēja līdz pirmajam simbolam

Pēdēja simbola indekss ir `[-1]`, pirmspēdējais ir `[-2]` un tā tālāk.

```python
text = 'Hello World'

print(text[-1]) # d
```

##### `len()` metode

Metode `len()` ļauj uzzināt `string` virknes garumu.

```python
text = 'Hello World'
print(len(text)) # 11
```

##### `string` nav maināms

> [!NOTE] Svarīgi!
> `string` datu tips nav maināms. Kā izveidoji teksta virkni tāda tā un paliks.

```python
text = 'Hello'
text[0] = 'R' # error!
```

Ja vēlies mainīt `string` virkni, **pārdefinē to:**

```python
text = 'Hello World' # old value
text = 'Albatross'   # new value
```

##### `string` apvienošana

Lai apvienot divas un vairākas `string` virknes, izmanto `+`.

```python
print('Encrypted text: ' + text)
```

##### Interpolācija

Interpolācija ļauj izmantot mainīgos teksta izvadā.

```python
print(f'Encrypted text: {text}')
```

#### `\n` jaunā rinda

Simbols `\n` ļauj izveidot jauno rindu.

```python
print(f'\nEncrypted text: {text}')
```

##### Diapazons

Var piekļūt pie `string` vērtībām, izmantojot diapazonu.

```python
string[start:stop:step]
```

- `start` - sākums, ieskaitot;
- `stop` - pēdējais indekss, neieskaitot;
- `step` - solis, pa cik simboliem pārvietoties.

Tāpatās var iet arī no `string` masīva beigām uz sākumu:

```python
# card_number = 4111111145551142
card_number_reversed = card_number[-1:-5:-1]
# card_number_reversed = 2411

# reverse all of card_number
card_number_reversed = card_number[::-1]
# 2411555411111114

# take an even (nepāra) digits
even_digits = card_number_reversed[1::2]
```

Kur:

- `-1` - no pēdējā elementa ieskaitot;
- `-5` - līdz `-5` elementam neieskaitot;
- `-1` - reverss, no beigām uz sākumu

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Navigācija - Python strukturēts]]
Nākama lapa >>> [[find() metode]]

---
### ⇄ Saistības

Avots >>> [Learn String Manipulation by Building a Cipher: Step 5 \| freeCodeCamp.org](https://www.freecodecamp.org/learn/scientific-computing-with-python/learn-string-manipulation-by-building-a-cipher/step-5)
Iepriekšēja lapa >>> [[Konsoles izvads, metode print]]
Nākama lapa >>> [[Metode type()]]

___