**Datums:** 2025-04-27   
**Laiks:** 22:01 
❚ **Tagi:** #OOP

⌬ **Objekts:**  `OOP`

---
### ⬢ Detalizēts apraksts
#### Tēma 1 - Ievads

> [!NOTE] Abstraktā klase
> Nepabeigta klase, kas var saturēt gan pilnas, gan abstraktas (tukšas) metodes; abstraktās metodes `<abstract>` jārealizē visās mantojošajās klasēs.

> [!NOTE] Interfeiss
> Pilnīgi abstrakts līgums ar obligāti realizējamām metodēm; mantošana tiek apzīmēta ar punktētu līniju `- - - >`.

> [!NOTE] new
> Slēpj bāzes klases metodi, izveidojot jaunu metodi ar tādu pašu nosaukumu, kas tiek izsaukta, ja mainīts objekta datutips.

> [!NOTE] override
> Pārraksta mantotās klases metodi; prasa, lai bāzes klasē metode būtu atzīmēta ar `virtual` vai `abstract`.
#### Tēma 2 - Abstraktās klases

Apzīmēšana: mantošana un abstraktās klases tiek zīmētas ar punktētu bultiņu `- - - >`.
Nosaukumu konvencija: abstraktām klasēm liek priekšā burtu `A` (piem., `AAuthentification`), interfeisiem – `I`.

```cs
internal abstract class AAuthentification
{
    protected string token;
    protected bool isValid;

    public AAuthentification() {
        token = "";
        isValid = false;
    }
	//abstraktā metode
    public abstract void Authentification();
    //parastas metodes
    public bool IsValid() => isValid;
    public string Token() => token;
}
```

No abstraktas klases tieši objektu nevar veidot - nepieciešama konkrēta klase, kas manto un realizē abstraktās metodes.

![[Pasted image 20250527184537.png]]
#### Tēma 3 - `new` un `override`

>**`new`** Slēpj bāzes klases metodi ar jaunu definīciju. Darbojas tikai tad, ja objekta datutips ir nomainīts uz atvasināto klasi.

>**`override`** Pilnībā pārraksta bāzes klases metodi. <mark style="background: #FFB86CA6;">Prasība:</mark> bāzes klases metodei jābūt atzīmētai ar `virtual` vai `abstract`.

Pārbaude, kādai klasei pieder objekts:

```cs
if (obj is Password) { … }
```
---
### ⚛ Secinājums/i

- **Abstraktā klase** - nepabeigta klase ar abstraktām un gatavām metodēm; objektu veidot nevar, tikai mantot.
- **Interfeiss** - pilnīgi abstrakts; visas metodes obligāti jārealizē; mantošana tiek zīmēta ar punktētu līniju.
- **`new`** - slēpj bāzes klases metodi ar jaunu versiju; darbojas pie datu tipa nomaiņas.
- **`override`** - pārraksta bāzes klases metodi, bāzes metode jābūt `virtual` vai `abstract`.
- **Objekta tipu** var pārbaudīt ar `is` operatoru (`if (obj is Password)`).

---
### ⇄ Saistības

Iepriekšēja lapa >>> [[Interfeiss un nosaukumvieta]]
Nākama lapa >>> [[Vairāku failu izmantošana vienā projekta ietvaros]]

---