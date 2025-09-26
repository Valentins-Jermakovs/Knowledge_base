___

**Datums:** 2025-08-02   
**Laiks:** 15:03 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### `try...except kosntrukcija`

Bloks `try` domāts, lai testēt kodu, kas potenciāli var izraisīt kļūdas.
Bloks `except` ļauj apstrādāt kļūdu.
Bloks `else` ļauj izpildīt kodu, ja kļūdu nav.
Bloks `finally` izpildās jebkurā gadījumā.

##### Kļūdas apstrādes piemērs

Šeit tiks izvadīts kļūdas paziņojums, jo mainīgais `x` nav definēts.

```python
try:
  print(x)
except:
  print("An exception occurred") 
```

##### Vairāku kļūdu apstrāde

`Python` valoda ļauj apstrādāt vairākas kļūdas

```python
#The try block will generate a NameError, because x is not defined:

try:
  print(x)
except NameError:
  print("Variable x is not defined")
except:
  print("Something else went wrong")
```

##### Else

Bloku `else` var izmantot koda izpildei, ja kļūdas nenotika.

```python
try:
  print("Hello")
except:
  print("Something went wrong")
else:
  print("Nothing went wrong") 

# Hello
# Nothing went wrong
```

##### Finally

Bloks `finally` izpildās neatkarīgi no rezultāta, tas nozīmē - vienmēr.

```python
try:
  print(x)
except:
  print("Something went wrong")
finally:
  print("The 'try except' is finished") 
```

##### Kļūdu ģenerācija

Kā `python` izstrādātājs, tu vari ģenerēt, izsaukt kļūdas patstāvīgi.

```python
x = -1

if x < 0:
  raise Exception("Sorry, no numbers below zero") 
```

```python
x = "hello"

if not type(x) is int:
  raise TypeError("Only integers are allowed") 
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Navigācija - Python strukturēts]]

---
### ⇄ Saistības

Avots >>> [Python Try Except](https://www.w3schools.com/python/python_try_except.asp)
Iepriekšēja lapa >>> [[Modulis math]]
Nākama lapa >>> [[Sevis veidota moduļa (faila) imports]]

___