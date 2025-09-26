**Datums:** 2025-04-27   
**Laiks:** 21:54 
❚ **Tagi:**  #OOP 

⌬ **Objekts:**  `OOP`

---
### ⬢ Detalizēts apraksts
#### Tēma 1 - Ievads

Interfeiss ir speciāla klase, kas definē metožu parakstus, kuras jārealizē mantojošajām klasēm. Nosaukumvieta (namespace) ļauj loģiski grupēt saistītas klases un izvairīties no nosaukumu konfliktiem.

> [!NOTE] Interfeiss
> Nosaka, kādas metodes klasei ir jāimplementē.

> [!NOTE] Interfeisa mantošana
> Klases īstenošana, kas pārņem interfeisā definētās metodes.

> [!NOTE] Nosaukumvieta
> Loģiska datu un tipu grupēšana, nodala vienādos nosaukumus.
#### Tēma 2 - Interfeiss

>Interfeiss ir “contracts” klases līmenī, kas satur vienīgi metožu signatūras.

```cs
interface IDrawable
{
    void Draw();
}
```
#### Tēma 3 - Interfeisa mantošana

>Klasēm, kas manto interfeisu, <mark style="background: #BBFABBA6;">jāimplementē visas tajā definētās metodes.</mark>

```cs
class Square : IDrawable
{
    int side;

    public Square(int side)
    {
        this.side = side;
    }

    public void Draw() //metode no interfeisa
    {
        // uzzīmē kvadrātu malas garumā side
        Console.WriteLine($"Drawing square with side {side}");
    }
}
```
#### Tēma 4 - Nosaukumvieta

>Grupē loģiski saistītas klases, lai novērstu nosaukumu kolīzijas un uzlabotu koda pārskatāmību.

```cs
namespace visualization
{
    interface IDrawable
    {
        void Draw();
    }
}

using visualization;

namespace geometric_figures
{
    class Line : IDrawable
    {
        int length;
        public Line(int length)
        {
            this.length = length;
        }

        public void Draw()
        {
            // uzzīmē līniju ar garumu length
            Console.WriteLine($"Drawing line of length {length}");
        }
    }
}
```

---
### ⚛ Secinājums/i

>Interfeisi nodrošina saskaņotu veidu, kā dažādas klases var realizēt kopīgas funkcijas, savukārt nosaukumvietas palīdz strukturēt kodu un novērst nosaukumu konfliktsituācijas.

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Mantošana un polimorfisms]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp OOP/Pamati/Abstraktās klases]]

---