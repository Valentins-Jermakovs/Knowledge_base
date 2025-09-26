___
**Datums:** 2025-07-09   
**Laiks:** 13:01 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Kods

```csharp
string pangram = "The quick brown fox jumps over the lazy dog";

/*
    Šī programma apgriež visus vārdus,
    uztaisa tiem reversu.
*/

string[] words = pangram.Split(" ");    // Izveido masīvu ar string elementiem
                                        // Elemti tiek atdalīti pēc " "
foreach (var item in words)
{
    Console.WriteLine(item);
}

Console.WriteLine();

string[] reversedMessage = new string [words.Length];   // Izveido masīvu ar garumu words.Length

/*
    Cikls, kas iterē pa words,
    izņem katru vārdu, apgriež un ieraksta masīvā reversedMessage
*/

for (int i = 0; i < words.Length; i++)
{
    char[] array = words[i].ToCharArray();
    Array.Reverse(array);
    reversedMessage[i] = new string(array);
}

/*
    Tā kā reversedMessage ir masīvs,
    tā elementus var atdalīt vienu no otra ar " ",
    izmantojot Joins().

    Apgriezti elementi ar " " starp tiem,
    tiek ierakstīti mainīgā result.
*/

string result = String.Join(" ", reversedMessage);
Console.WriteLine(result);
```

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Modulis 4/Masīvu metodes]]
Nākama lapa >>> [[Programma, kas pievieno tagus]]
___