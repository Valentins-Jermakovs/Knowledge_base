___

**Datums:** 2025-08-07
**Laiks:** 11:07
❚ **Tagi:** #html
⌬ **Priekšmets:**  `HTML`

---
### ⬢ Detalizēts apraksts
#### `<input>` tags

> [!NOTE] `<input>`
> Šīs tags paredzēts lietotāja ievadam. Tas ļauj ievadīt tekstu, paroli, augšupielādēt failus un vēl daudz citu lietu, par ko aprakstīts zemāk.

Taga struktūra:

```html
<input type='norādi_tipu' placeholder='teksts_ko_redz_lietotājs'>
```

Tags `<input>` ir `type`, kas norāda, kas par ievada tipu tas ir. Pastāv vairāki šādi tipi:

- `type='text'` - standarta teksta ievades lauks;
- `type='password'` - paroles ievada lauks, simboli tiek paslēpti;
- `type='date'` - izkrītošais kalendārs, kur lietotājs izvēlas datumu;
- `type='time'` - lietotājs ievada/izvēlas laiku;
- `type='color'` - color picker;
- `type='file'` - šīs tips ļauj lietotājam augšupielādēt failus no savas ierīces;
- `type='checkbox'` - šis tips ļauj izveidot `checkboxus`, elementus, kurus var atzīmēt kā izvēlētos (var atzīmēt vairākus elementus);
- `type='radio'` - šis tips ļauj izveidot sarakstu, kur lietotājs var izvēlēties tikai vienu elementu.

Zemāk tiek aprakstīts `type='file'` un tā īpatnības.

```html
<input type='file' accept='image/*,.pdf' multiple>
```

Lauks `accept` ļauj izstrādātājam noteikt, kāda tipa failus lietotājam ir atļauts augšupielādēt. Atribūts `multiple` nav obligāts, tas vienkārši ļauj augšupielādēt vairākus failus par vienu reizi.

Vairāk par `accept`:

- `audio/*` - ļauj augšupielādēt jebkura audio tipa failu;
- `video/*` - ļauj augšupielādēt jebkura video tipa failu;
- `image/*` - ļauj augšupielādēt jebkura attēla tipa failu;
- `.jpg, .pdf, .doc` - šāds pieraksts ļauj norādīt konkrētus failu tipus.

#### Papildinājums

`<input>` kopumā veido formas `<form>`.

```html
<!DOCTYPE html>
<html>
<body>

<h1>Display Radio Buttons</h1>

<form action="/action_page.php">
  <p>Please select your favorite Web language:</p>
  <input type="radio" id="html" name="fav_language" value="HTML">
  <label for="html">HTML</label><br>
  <input type="radio" id="css" name="fav_language" value="CSS">
  <label for="css">CSS</label><br>
  <input type="radio" id="javascript" name="fav_language" value="JavaScript">
  <label for="javascript">JavaScript</label>

  <br>  

  <p>Please select your age:</p>
  <input type="radio" id="age1" name="age" value="30">
  <label for="age1">0 - 30</label><br>
  <input type="radio" id="age2" name="age" value="60">
  <label for="age2">31 - 60</label><br>  
  <input type="radio" id="age3" name="age" value="100">
  <label for="age3">61 - 100</label><br><br>
  <input type="submit" value="Submit">
</form>

</body>
</html>
```

---
### ⇄ Saistības

Avots >>> [\<input type="file"\> - HTML \| MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/input/file)
Iepriekšēja lapa >>> [[Tags img]]
Nākama lapa >>> [[Tags a]]

---