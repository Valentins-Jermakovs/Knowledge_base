___

**Datums:** 2025-09-21
**Laiks:** 18:20
❚ **Tagi:** #kotlin 

---
# Attēla faila pievienošana projektam

Lai pievienot attēla failu projektam, veic šādas darbības:

1. **Atver Resource Manager.** Android Studio izvēlne: View > Tool Windows > Resource Manager.
2. **Importē attēlu.** Resource Manager logā → spied `+` (Add resources to the module) → Import Drawables. Atrodi failu un spied Open. Parādās dialogs Import Drawables.
3. **Iestati blīvuma parametrus** - Nolaižamajā izvēlnē QUALIFIER TYPE izvēlies → Density. Pie VALUE izvēlies → No Density. (Tas nozīmē, ka attēls netiks mērogots dažādās ekrānu izšķirtspējās)

> [!NOTE] 💡 Kāpēc?
> Android ierīcēm ir dažādas pikseļu blīvuma vērtības (dpi). Ja attēls tiek mērogots automātiski, tas var kļūt izplūdis vai pat izraisīt atmiņas kļūdas. Lieliem attēliem (foni, fotogrāfijas) izmanto drawable-nodpi mapi, lai tie netiktu pārveidoti.

4. **Importēšana.** Spied Next. Android Studio parādīs, ka attēls tiks ievietots mapē drawable-nodpi. Spied Import.
5. **Rezultāts.** Android Studio izveidos mapi drawable-nodpi un tur ievietos tavu failu. Attēls būs redzams sadaļā Drawable Resource Manager logā. Projektā: app > res > drawable-nodpi > tavs_fails.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - Add images to your Android app]]
Nākama lapa >>> [[Attēla attēlošana uz ekrāna]]

---