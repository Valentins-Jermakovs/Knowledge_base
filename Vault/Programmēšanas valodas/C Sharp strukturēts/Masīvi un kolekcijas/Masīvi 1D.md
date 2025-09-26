___

**Datums:** 2025-08-04   
**Laiks:** 18:52 

❚ **Tagi:** #C_Sharp 
⌬ **Priekšmets:**  `C#`

---
### ⬢ Detalizēts apraksts
#### `1D` masīvi

##### `1D` masīva deklarēšana

```csharp
// Declare a single-dimensional array of 5 integers.
int[] array1 = new int[5];

// Declare and set array element values.
int[] array2 = {1, 2, 3, 4, 5, 6};
```

```csharp
int[] array = new int[5];
string[] weekDays = {"Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"};

Console.WriteLine(weekDays[0]);
Console.WriteLine(weekDays[1]);
Console.WriteLine(weekDays[2]);
Console.WriteLine(weekDays[3]);
Console.WriteLine(weekDays[4]);
Console.WriteLine(weekDays[5]);
Console.WriteLine(weekDays[6]);

/*Output:
Sun
Mon
Tue
Wed
Thu
Fri
Sat
*/
```

`1D` masīvu nodošana funkcijai:

```csharp
class ArrayExample
{
    static void DisplayArray(string[] arr) => Console.WriteLine(string.Join(" ", arr));

    // Change the array by reversing its elements.
    static void ChangeArray(string[] arr) => Array.Reverse(arr);

    static void ChangeArrayElements(string[] arr)
    {
        // Change the value of the first three array elements.
        arr[0] = "Mon";
        arr[1] = "Wed";
        arr[2] = "Fri";
    }

    static void Main()
    {
        // Declare and initialize an array.
        string[] weekDays = {"Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"};
        // Display the array elements.
        DisplayArray(weekDays);
        Console.WriteLine();

        // Reverse the array.
        ChangeArray(weekDays);
        // Display the array again to verify that it stays reversed.
        Console.WriteLine("Array weekDays after the call to ChangeArray:");
        DisplayArray(weekDays);
        Console.WriteLine();

        // Assign new values to individual array elements.
        ChangeArrayElements(weekDays);
        // Display the array again to verify that it has changed.
        Console.WriteLine("Array weekDays after the call to ChangeArrayElements:");
        DisplayArray(weekDays);
    }
}
// The example displays the following output:
//         Sun Mon Tue Wed Thu Fri Sat
//
//        Array weekDays after the call to ChangeArray:
//        Sat Fri Thu Wed Tue Mon Sun
//
//        Array weekDays after the call to ChangeArrayElements:
//        Mon Wed Fri Wed Tue Mon Sun
```

Operators `^` ļauj ātri un vienkārši iegūt masīva pēdējos elementus:

```csharp
int[] numbers = {1, 2, 3, 5};
 
Console.WriteLine(numbers[^1]);  // 5 - первый с конца или последний элемент
Console.WriteLine(numbers[^2]);  // 3 - второй с конца или предпоследний элемент
Console.WriteLine(numbers[^3]);  // 2 - третий элемент с конца
```

---
### ⇄ Saistības

Avots >>> [Тип ссылки массива - C# reference \| Microsoft Learn](https://learn.microsoft.com/ru-ru/dotnet/csharp/language-reference/builtin-types/arrays)
Iepriekšēja lapa >>> [[Navigācija - C Sharp strukturēts]]
Nākama lapa >>> [[Programmēšanas valodas/C Sharp strukturēts/Masīvi un kolekcijas/Masīvi 2D|Masīvi 2D]]

___