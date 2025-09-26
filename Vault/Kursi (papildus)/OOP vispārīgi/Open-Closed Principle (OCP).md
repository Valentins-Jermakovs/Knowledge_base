⏲ **Datums:** 2025-04-27   
⏲ **Laiks:** 22:19 
❚ **Tagi:**  #OOP

⌬ **Objekts:**  `OOP`

---
### ⬢ Detalizēts apraksts
#### Tēma 1 - Ievads
Princips nosaka, ka klasei jābūt atvērtai paplašināšanai un aizvertai priekš modifikācijām. Tas nozīmē, ka, mainoties prasībām, esošo klasi nevajadzētu modificēt - jaunu funkcionalitāti pievieno, paplašinot risinājumu ar jauniem komponentiem.

> [!NOTE] OCP
> Moduļiem un klasēm jābūt atvērtām paplašināšanai, bet slēgtām priekš modifikācijām.
#### Tēma 2 - Vienkāršie piemēri
**Slikts piemērs:** visas formas apstrāde vienā klasē, katram veidam jāveic izmaiņas esošajā kodā.
```cs
public class AreaCalculator {
    public double CalculateCircleArea(double radius) {
        return Math.PI * radius * radius;
    }
    public double CalculateRectangleArea(double width, double height) {
        return width * height;
    }
    // Ja jāaprēķina, piemēram, trijstūra laukums, jārediģē šī klase
}
```
**Problēma:** katru reizi, kad parādās jauna forma, jāmodificē `AreaCalculator` klase - pārkāpj OCP.

**Atvērtā versija - izmantojot interfeisu:**
Definējam `IShape` interfeisu ar metodi `Area()`, un katrai formai veidojam savu klasi.
```cs
public interface IShape {
    double Area();
}

public class Circle : IShape {
    private readonly double radius;
    public Circle(double radius) { this.radius = radius; }
    public double Area() => Math.PI * radius * radius;
}

public class Rectangle : IShape {
    private readonly double width, height;
    public Rectangle(double width, double height) { this.width = width; this.height = height; }
    public double Area() => width * height;
}

public class AreaProcessor {
    // Apstrāde visiem veidiem, izmantojot interfeisu
    public double TotalArea(IEnumerable<IShape> shapes) {
        double sum = 0;
        foreach (var shape in shapes)
            sum += shape.Area();
        return sum;
    }
}
```
**Izmantošana:**
```cs
var shapes = new IShape[] {
    new Circle(5),
    new Rectangle(4, 6)
};
var processor = new AreaProcessor();
var total = processor.TotalArea(shapes);
Console.WriteLine($"Total area: {total}");
```

>**Priekšrocības:**
 >   1. Jauna forma - pietiek pievienot jaunu klasi, kas implementē `IShape`;
>    2. `AreaProcessor` nav jāmaina: kods ir atvērts paplašināšanai, slēgts modifikācijām.

---
### ⚛ Secinājums/i
Interfeisa izmantošana parāda OCP: jauna funkcionalitāte (jauna forma) tiek pievienota ar jaunu klasi, neietekmējot esošo kodu.

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Single Responsibility Principle (SRP)]]
Nākama lapa >>> [[Liskov Substitution Principle (LSP)]]

---