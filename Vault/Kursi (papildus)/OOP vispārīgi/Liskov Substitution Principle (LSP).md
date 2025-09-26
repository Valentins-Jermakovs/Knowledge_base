⏲ **Datums:** 2025-05-08   
⏲ **Laiks:** 21:07 
❚ **Tagi:**  #OOP 

⌬ **Objekts:**  `OOP`

---
### ⬢ Detalizēts apraksts
#### Ievads
Princips ir nosaukts pēc autores vārda (Barbara Liskov), kura to noformulēja. Princips
nosaka, ka funkcijai, kas apstrādā vecāka klasi (parent class) jāstrādā korekti arī ar
klases bērniem (child classes).
#### Slikts piemērs
```cs
public class Taisnstūris
{
    public virtual int Platums { get; set; }
    public virtual int Augstums { get; set; }

    public int AprēķinātLaukumu()
    {
        return Platums * Augstums;
    }
}

public class Kvadrāts : Taisnstūris
{
    public override int Platums
    {
        set
        {
            base.Platums = value;
            base.Augstums = value;
        }
    }

    public override int Augstums
    {
        set
        {
            base.Platums = value;
            base.Augstums = value;
        }
    }
}

class Program
{
    static void Main()
    {
        Taisnstūris figūra = new Kvadrāts();
        figūra.Platums = 5;
        figūra.Augstums = 10;

        // Sagaidām, ka laukums būs 5 * 10 = 50, bet patiesībā tas būs 10 * 10 = 100
        Console.WriteLine(figūra.AprēķinātLaukumu()); // Kļūda!
    }
}
```
**Problēma:** Kvadrāts pārraksta uzvedību un maina loģiku, ko sagaida `Taisnstūris`. Ja kvadrāts aizstāj taisnstūri, programma sāk darboties nepareizi. Tādējādi tiek pārkāpts LSP.
#### Labs piemērs
```cs
public abstract class Figūra
{
    public abstract int AprēķinātLaukumu();
}

public class Taisnstūris : Figūra
{
    public int Platums { get; set; }
    public int Augstums { get; set; }

    public override int AprēķinātLaukumu()
    {
        return Platums * Augstums;
    }
}

public class Kvadrāts : Figūra
{
    public int Mala { get; set; }

    public override int AprēķinātLaukumu()
    {
        return Mala * Mala;
    }
}

class Program
{
    static void Main()
    {
        List<Figūra> figūras = new List<Figūra>
        {
            new Taisnstūris { Platums = 5, Augstums = 10 },
            new Kvadrāts { Mala = 5 }
        };

        foreach (var figūra in figūras)
        {
            Console.WriteLine(figūra.AprēķinātLaukumu());
        }
    }
}
```
**Priekšrocība:** Katrai figūrai ir sava loģika, un tās **var aizvietot viena otru bez blakus efektiem**. LSP tiek ievērots.

---
### ⚛ Secinājums/i
> Princips nosaka, ka funkcijai, kas apstrādā vecāka klasi (parent class) jāstrādā korekti arī
> ar klases bērniem (child classes).

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Open-Closed Principle (OCP)]]
Nākama lapa >>> [[Interface Segregation Principle]]

---