___

**Datums:** 2025-09-20
**Laiks:** 15:27
❚ **Tagi:** #back-end #NET 

---
### Migrācijas

Migrācijas attiecināmas uz:

- klašu pievienošanu;
- klašu modifikācijām;
- klašu dzēšanu.

Migrācijas nepieciešams veikt ik pēc katras moduļa (tabulas) vai DB failu, piem., `context.cs` atjaunošanas.


> [!NOTE] Ieteikums
> Vienmēr strādājiet pie nelielām izmaiņām un mazām migrācijām. Vienmēr veic migrācijas ik pēc katra neliela uzdevuma.

Komandas, ko jāievada `Package Manager` konsolē:

- `enable-migrations` - ieslēdz migrācijas, lai gan tagad tās esot ieslēgtas pēc noklusējuma, tomēr ieteicams ievadīt;
- `add-migration migrācijasNosaukums`  - veic pašu migrāciju, nosaukumus norādi angliski.

Migrāciju komandai ir arī parametri:

```
add-migration name atslēga
```

Atslēgas:

- `-IgnoreChanges` (vajadzīgs, kad veici izmaiņas pašā DB, bet neesi veicis jaunas migrācijas pašā projektā);
- `-Force` (ignorē DB un pārraksta to, lai atbilstu projektam).

**Ja izdzēsi migrāciju projektā, izdzēs to arī no DB!**

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Projekta veidošana]]
Nākama lapa >>> [[DB atjaunināšana]]

---