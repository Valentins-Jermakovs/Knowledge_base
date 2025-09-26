___
**Datums:** 2025-07-09   
**Laiks:** 13:21 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Kods

```csharp
string orderStream = "B123,C234,A345,C15,B177,G3003,C235,B179";

string[] orderStreamArray = orderStream.Split(",");     // Sadala pa elementiem
Array.Sort(orderStreamArray);

for (int i = 0; i < orderStreamArray.Length; i++)
{
    char[] word = orderStreamArray[i].ToCharArray();
    string newWord = new string(word);

    if (word.Length != 4)
    {
        Console.WriteLine($"{newWord}\t - Error");
    }
    else
    {
        Console.WriteLine($"{newWord}");
    }
}
```

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Programma, kas pievieno tagus]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp/Modulis 4/Composite Formatting]]
___