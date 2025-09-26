___

**Datums:** 2025-09-21
**Laiks:** 19:24
❚ **Tagi:** #kotlin 

---
# Teksta izvietošana resursu failā

 Android Studio ļauj **izvilkt tekstu uz string resursu**:
 
1. Atlasīt tekstu `Happy Birthday Sam!` kodā;
2. Klikšķināt uz **bulb (gaismas spuldzes ikonas)**;
3. Izvēlēties **Extract string resource**.
 
Dialogā:
- **Resource name** → piemēram, `happy_birthday_text` (mazie burti, vārdi ar underscore);
- **Resource value** → paša teksta saturs `"Happy Birthday Sam!"`;  

Rezultātā kodā teksts tiek aizvietots ar:

```kotlin
message = stringResource(R.string.happy_birthday_text)
```

### String resursu fails

- Resursi atrodas `res/values/strings.xml`
- Piemērs pēc abu tekstu izvilkšanas:

```xml
<resources>
    <string name="app_name">Happy Birthday</string>
    <string name="happy_birthday_text">Happy Birthday Sam!</string>
    <string name="signature_text">From Emma</string>
</resources>
```

*Piezīme. Šādu lietu ieteicams veikt, lai nākotnē būtu vienkāršāk tulkot programmu citās valodās.*

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Paddingi]]
Nākama lapa >>> [[Navigācija - Add images to your Android app]]

---