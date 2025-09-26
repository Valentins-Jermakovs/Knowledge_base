___

**Datums:** 2025-08-07
**Laiks:** 16:03
❚ **Tagi:** #html
⌬ **Priekšmets:**  `HTML`

---
### ⬢ Detalizēts apraksts
#### `<label>` tags

Šī tēma pārklājas ar `<input>` tagu >>> [[Tags input]].
Tags `<label>` tiek izmantots, lai padarītu `user experience` un pieejamību labāku. `<label>` tiek lietots kopā ar `<input>` kā skaidrojums, norāde lietotājam.

```html
<h2>Register</h2>
<label for='name'>Your Name:</label>
<input placeholder='E.g Alexander Rybak' id='name'>
```

Kā var redzēt piemēra, šeit tiek izmantots `id`. Šādi `html` elementam tiek piešķirts unikāls identifikators, kas tiek iedots tagam `<label>`, tādējādi šie 2 elementi tiek savā starpā saistīti.

```html
<!DOCTYPE html>
<html>
<body>

<h1>Show Checkboxes</h1>

<form action="/action_page.php">
  <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
  <label for="vehicle1"> I have a bike</label><br>
  <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
  <label for="vehicle2"> I have a car</label><br>
  <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
  <label for="vehicle3"> I have a boat</label><br><br>
  <input type="submit" value="Submit">
</form>

</body>
</html>
```

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[The Description List]]
Nākama lapa >>> [[Par time]]

---