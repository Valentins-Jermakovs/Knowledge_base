⏲ **Datums:** 2025-04-27   
⏲ **Laiks:** 22:16 
❚ **Tagi:** #OOP

⌬ **Objekts:**  `OOP`

---
### ⬢ Detalizēts apraksts
#### Tēma 1 - Ievads
SRP nosaka, ka katrai klasei jābūt tikai vienai atbildībai vai vienam uzdevumam. Tas palīdz saglabāt kodu skaidru un viegli uzturamu.

> [!NOTE] Single Responsibility Principle (SRP)
> Katras klases vai moduļa atbildība ir ierobežota ar vienu, konkrētu uzdevumu.
#### Tēma 2 - Single Responsibility Principle
> Viena klase = viena funkcija

**Ieguvumi:**
- Samazina atkarības starp komponentēm;
- Padara testēšanu un refaktorēšanu vienkāršāku;
- Atvieglo koda paplašināšanu un uzturēšanu.

**Slikts piemērs - viena klase atbild par vairākām lietām:**
```cs
internal class ReportManager {
    public void GenerateReport() {
        // ģenerē atskaiti
    }
    public void SaveToFile(string path) {
        // saglabā failā
    }
    public void SendEmail(string address) {
        // nosūta e-pastu
    }
}
```
*Šajā klasē apvienotas trīs atbildības - atskaites ģenerēšana, saglabāšana un nosūtīšana.*

**Labs piemērs - atdalītas atbildības:**
```cs
internal class ReportGenerator {
    public string Generate() {
        // ģenerē un atgriež atskaites datus
        return "Report Data";
    }
}

internal class FileSaver {
    public void Save(string content, string path) {
        File.WriteAllText(path, content);
        // saglabā failā
    }
}

internal class EmailSender {
    public void Send(string content, string address) {
        // sūta e-pastu ar saturu
    }
}
```
*Katram modulim sava atbildība: ģenerēšana, saglabāšana, nosūtīšana.*

---
### ⚛ Secinājums/i
> SRP principa ievērošana palīdz sadalīt kodu loģiskos, vienkāršos komponentos, kas uzlabo uzturējamību un testēšanas iespējas.

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Navigācija - OOP vispārīgi]]
Nākama lapa >>> [[Open-Closed Principle (OCP)]]

---