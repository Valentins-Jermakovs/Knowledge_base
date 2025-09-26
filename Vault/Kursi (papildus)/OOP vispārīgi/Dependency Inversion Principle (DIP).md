⏲ **Datums:** 2025-05-08   
⏲ **Laiks:** 21:08 
❚ **Tagi:**  #OOP 

⌬ **Objekts:**  `OOP`

---
### ⬢ Detalizēts apraksts
#### Ievads
Ja burtiski tulkot “Atkārību inversijas princips”, kas noteic, ka funkcijām labāk būt
atkārīgām no abstrakcijām (interfeisiem un abstraktām klasēm) nevis konkrētām
klasēm.
#### Slikts piemērs
```cs
public class FailsRakstītājs
{
    public void Rakstīt(string ziņa)
    {
        // Reāli raksta uz failu (šeit vienkāršoti)
        Console.WriteLine("Rakstu failā: " + ziņa);
    }
}

public class ZiņojumuServiss
{
    private FailsRakstītājs rakstītājs = new FailsRakstītājs();

    public void Sūtīt(string ziņa)
    {
        rakstītājs.Rakstīt(ziņa);
    }
}
```
**Problēma:** `ZiņojumuServiss` ir **cieši saistīts** ar `FailsRakstītājs`. Ja gribi izmantot, piemēram, `EpastaRakstītājs`, tev jāmaina kods iekš `ZiņojumuServiss`.
#### Labs piemērs
```cs
public interface IRakstītājs
{
    void Rakstīt(string ziņa);
}

public class FailsRakstītājs : IRakstītājs
{
    public void Rakstīt(string ziņa)
    {
        Console.WriteLine("Rakstu failā: " + ziņa);
    }
}

public class EpastaRakstītājs : IRakstītājs
{
    public void Rakstīt(string ziņa)
    {
        Console.WriteLine("Sūtu e-pastu: " + ziņa);
    }
}

public class ZiņojumuServiss
{
    private readonly IRakstītājs rakstītājs;

    public ZiņojumuServiss(IRakstītājs rakstītājs)
    {
        this.rakstītājs = rakstītājs;
    }

    public void Sūtīt(string ziņa)
    {
        rakstītājs.Rakstīt(ziņa);
    }
}

class Program
{
    static void Main()
    {
        IRakstītājs rakstītājs = new EpastaRakstītājs(); // Vai new FailsRakstītājs();
        var serviss = new ZiņojumuServiss(rakstītājs);
        serviss.Sūtīt("Sveiciens no DIP piemēra!");
    }
}
```
**Priekšrocība:** `ZiņojumuServiss` **nezina**, kur rakstīs ziņu — failā, e-pastā vai citur. Viss, kas viņam jādara — izmantot **interfeisu** `IRakstītājs`. Vēlāk tu vari **injicēt jebkuru realizāciju** bez izmaiņām servisa klasē.

---
### ⚛ Secinājums/i
>Funkcijām labāk būt atkarīgām no abstrakcijām (interfeisiem un abstraktām klasēm) nevis konkrētām klasēm.

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Interface Segregation Principle]]
Nākama lapa >>> [[Navigācija - OOP vispārīgi]]

---