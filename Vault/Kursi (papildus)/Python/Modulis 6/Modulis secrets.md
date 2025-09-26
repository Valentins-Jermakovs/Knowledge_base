___

**Datums:** 2025-07-30   
**Laiks:** 13:01 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Modulis

Modulis `secrets` tiek izmantots, lai ģenerētu paroles, tokenus un citas drošības lietas.
Biežāk no tā tiek izmantota metode `choice()`. Tā atgriež vienu nejaušu simbolu no simbolu komplekta, kas tiek nodots.

```python
import re
import secrets
import string


def generate_password(length=16, nums=1, special_chars=1, uppercase=1, lowercase=1):

    # Define the possible characters for the password
    letters = string.ascii_letters
    digits = string.digits
    symbols = string.punctuation

    # Combine all characters
    all_characters = letters + digits + symbols

    while True:
        password = ''
        # Generate password
        for _ in range(length):
            password += secrets.choice(all_characters) # <- Šeit!
```

---
### ⇄ Saistības (strukturēts)

Iepriekšēja lapa >>> [[Modulis random]]
Nākama lapa >>> [[Modulis re]]

---
### ⇄ Saistības

Avots >>> [Python \| Модуль secrets](https://metanit.com/python/tutorial/6.9.php)
Iepriekšēja lapa >>> [[Modulis random]]
Nākama lapa >>> [[Modulis string]]

___