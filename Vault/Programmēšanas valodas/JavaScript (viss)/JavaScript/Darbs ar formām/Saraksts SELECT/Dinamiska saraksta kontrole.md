___

**Datums:** 2025-08-25
**Laiks:** 15:38
❚ **Tagi:** #javascript 
⌬ **Priekšmets:**  `JS`

---
### ⬢ Detalizēts apraksts
#### Dinamiska saraksta kontrole

Īpašība `selectedIndex` ļauj nodot izvēlēto saraksta elementu.
Piemērs, kā pievienot un dzēst saraksta elementus:

```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8" />
</head>

<body>
    <form name="myForm">
        <select name="language" size="5">
            <option value="JS" selected="selected">JavaScript</option>
            <option value="Java">Java</option>
            <option value="CS">C#</option>
            <option value="CPP">C++</option>
        </select>
        <p><input type="text" name="textInput" placeholder="Введите текст" /></p>
        <p><input type="text" name="valueInput" placeholder="Введите значение" /></p>
        <p>
            <input type="button" name="addButton" value="Добавить" />
            <input type="button" name="removeButton" value="Удалить" />
        </p>
    </form>

    <script>
        const myForm = document.myForm;
        const addButton = myForm.addButton,
            removeButton = myForm.removeButton,
            languagesSelect = myForm.language;
        // обработчик добавления элемента
        function addOption() {
            // получаем текст для элемента
            const text = myForm.textInput.value;
            // получаем значение для элемента
            const value = myForm.valueInput.value;
            // создаем новый элемента
            const newOption = new Option(text, value);
            languagesSelect.add(newOption);
        }
        // обработчик удаления элемент
        function removeOption() {

            const selectedIndex = languagesSelect.options.selectedIndex;
            // удаляем элемент 
            languagesSelect.remove(selectedIndex);
        }

        addButton.addEventListener("click", addOption);
        removeButton.addEventListener("click", removeOption);
    </script>
</body>

</html>
```

Koda rinda, kas pievieno elementu:

```js
languagesSelect.add(newOption);
```

Koda rinda, kas dzēš elementu:

```js
languagesSelect.remove(selectedIndex);
```

---
### ⇄ Saistības

Avots >>> [JavaScript \| Список select](https://metanit.com/web/javascript/10.5.php)
Iepriekšēja lapa >>> [[Saraksta izveide]]
Nākama lapa >>> [[Izvēles apstrāde]]

---