___
**Datums:** 2025-07-06   
**Laiks:** 13:32 
❚ **Tagi:** #C_Sharp 
⌬ **Kurss:**  `C#`

---
### ⬢ Detalizēts apraksts
#### Kods

```csharp
using System;



// initialize variables - graded assignments 
int examAssignments = 5;

int[] sophia = [90, 86, 87, 98, 100, 94, 90];
int[] andrew = [92, 89, 81, 96, 90, 89];
int[] emma = [90, 85, 87, 98, 68, 89, 89, 89];
int[] logan = [90, 95, 87, 88, 96, 96];
int[] becky = [92, 91, 90, 91, 92, 92, 92];
int[] chris = [84, 86, 88, 90, 92, 94, 96, 98];
int[] eric = [80, 90, 100, 80, 90, 100, 80, 90];
int[] gregor = [91, 91, 91, 91, 91, 91, 91];  

// Student names
string[] studentNames = ["Sophia", "Andrew", "Emma", "Logan", "Becky", "Chris", "Eric", "Gregor"];

int[] studentScores = new int[10];
string currentStudentLetterGrade = "";

Console.WriteLine("Student\t\tGrade\n");
foreach (string name in studentNames)
{
    string currentStudent = name;
    if (currentStudent == "Sophia")
    {
        studentScores = sophia;
    }
    else if (currentStudent == "Andrew")
    {
        studentScores = andrew;
    }
    else if (currentStudent == "Emma")
    {
        studentScores = emma;
    }
    else if (currentStudent == "Logan")
    {
        studentScores = logan;
    }
    else if (currentStudent == "Becky")
    {
        studentScores = becky;
    }
    else if (currentStudent == "Chris")
    {
        studentScores = chris;
    }
    else if (currentStudent == "Eric")
    {
        studentScores = eric;
    }
    else if (currentStudent == "Gregor")
    {
        studentScores = gregor;
    }
    else
        continue;

    
    int sumAssigmentScore = 0;
    decimal currentStudentGrade = 0;
    int gradedAssignments = 0;

    foreach (int score in studentScores)
    {
        gradedAssignments++;


        if (gradedAssignments <= examAssignments)
        {
            sumAssigmentScore += score;
        }
        else
        {
            sumAssigmentScore += score / 10;
        }
    }

    currentStudentGrade = (decimal)sumAssigmentScore / examAssignments;
    if (currentStudentGrade >= 97)
        currentStudentLetterGrade = "A+";
    else if (currentStudentGrade >= 93)
        currentStudentLetterGrade = "A";
    else if (currentStudentGrade >= 90)
        currentStudentLetterGrade = "A-";
    else if (currentStudentGrade >= 87)
        currentStudentLetterGrade = "B+";
    else if (currentStudentGrade >= 83)
        currentStudentLetterGrade = "B";
    else if (currentStudentGrade >= 80)
        currentStudentLetterGrade = "B-";
    else if (currentStudentGrade >= 77)
        currentStudentLetterGrade = "C+";
    else if (currentStudentGrade >= 73)
        currentStudentLetterGrade = "C";
    else if (currentStudentGrade >= 70)
        currentStudentLetterGrade = "C-";
    else if (currentStudentGrade >= 67)
        currentStudentLetterGrade = "D+";
    else if (currentStudentGrade >= 63)
        currentStudentLetterGrade = "D";
    else if (currentStudentGrade >= 60)
        currentStudentLetterGrade = "D-";
    else
        currentStudentLetterGrade = "F";

    Console.WriteLine($"{currentStudent}\t\t{currentStudentGrade}\t{currentStudentLetterGrade}");
}

Console.WriteLine("Press the Enter key to continue");
Console.ReadLine();
```

`Ctrl + F` atrast ievadīto tekstu.
`Ctrl + H` aizvietot atrasto ar jauno.

Links turpināšanai >>> [Create and Run Simple C# Console Applications - Challenge Project - Develop foreach and if-elseif-else Structures to Process Array Data in C# \| Learn \| freeCodeCamp.org](https://www.freecodecamp.org/learn/foundational-c-sharp-with-microsoft/create-and-run-simple-c-sharp-console-applications/challenge-project-develop-foreach-and-if-elseif-else-structures-to-process-array-data-in-c-sharp)

---
### ⇄ Saistības
Iepriekšēja lapa >>> [[Kursi (papildus)/C Sharp/Modulis 2/Komentāri]]
Nākama lapa >>> [[Kursi (papildus)/C Sharp/Modulis 2/Loģiskā noliegšana]]
___