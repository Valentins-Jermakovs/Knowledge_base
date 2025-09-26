___
**Datums:** 2025-07-07   
**Laiks:** 14:02 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Kods

```csharp
string[] myStrings = new string[2] {
    "I like pizza. I like roast chicken. I like salad.",
    "I like all three of the menu choices." 
};

int periodLocation = 0;                         // Saglabā punkta koordināti

for (int i = 0; i < myStrings.Length; i++)      // Iterē pa teikumiem
{
    string myString = myStrings[i];             // Saglabā teikumu
    periodLocation = myString.IndexOf(".");     // Atrod punktu

    while (periodLocation != -1)                // Ja punkts eksistē
    {
        /*
            Sākumā tas izgriež no myString teikumu līdz punktam,
            atmet `spaces` no kreisās puses.

            Izvada konsolē izgriezto teksta fragmentu

            Izdzēš izvadīto teksta fragmentu no myString,
            meklē nākamo punktu.

            Cikls darbojas tik ilgi, kamēr netiek izdzēsti punkti.
        */
        string sentence = myString.Substring(0, periodLocation).TrimStart();
        Console.WriteLine(sentence);

        myString = myString.Remove(0, periodLocation + 1);

        periodLocation = myString.IndexOf(".");
    }
}
```

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Modulis 3/Lietotāja ievada apstrāde]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp/Modulis 4/int datu tips]]
___