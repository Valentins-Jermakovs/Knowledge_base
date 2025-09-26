___

**Datums:** 2025-08-04   
**Laiks:** 18:08 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Mainīgie un to deklarācija


> [!NOTE] Variable
> A **variable** is a container for storing a type of value. Variables are important because their values can change, or vary, throughout the execution of a program. Variables can be assigned, read, and changed.

`C#` valodā izmanto stilu `camelCase`.

Variable names should use **camel case**, which is a style of writing that uses a lower-case letter at the beginning of the first word and an upper-case letter at the beginning of each subsequent word. For example, `string thisIsCamelCase;`.

```csharp
char userOption;

int gameScore;

decimal particlesPerMillion;

bool processedCustomer;
```

Vienkāršs teksta izvads

```csharp
string firstName;
firstName = "Bob";

Console.WriteLine(firstName);
```

#### Mainīgais `var`

`var` tas ir tāds mainīgais, kuram tiek noteikts tā datu tips, kad to deklarē.

```csharp
var message = "Hello!";
var letter = 'a';
var numbre = 1;
```

Pēc šāda mainīga deklarēšanas, tam tiek piešķirts datu tips, atbilstoši tam, kas tiek tajā ierakstīts. <mark style="background: #ADCCFFA6;">Un mainīt datu tipu nākotnē nevar.</mark> Šāds mainīgais tiek izmantots dinamiskai izstrādei.

---
### ⇄ Saistības

Avots >>> [Declare variables - Training \| Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/csharp-literals-variables/3-declaring-variables)
Iepriekšēja lapa >>> [[Navigācija - C Sharp strukturēts]]
Nākama lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Mainīgie un datu tipi/int datu tips|int datu tips]]

___