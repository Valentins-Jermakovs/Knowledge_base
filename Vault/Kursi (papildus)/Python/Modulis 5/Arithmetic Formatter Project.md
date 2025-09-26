___
**Datums:** 2025-07-28   
**Laiks:** 18:53 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Programmas kods

```python
def arithmetic_arranger(problems, show_answers=False):

    first_line = []
    operator_line = []
    second_line = []

    ##################### Check the problems ######################
    if len(problems) > 5:
      return 'Error: Too many problems.'
    
    for problem in problems:
       parts = problem.split()

       first_n = parts[0]
       operator = parts[1]
       second_n = parts[2]

       if operator in ['*','/']:
          return "Error: Operator must be '+' or '-'."
       
       if not first_n.isdigit() or not second_n.isdigit():
          return 'Error: Numbers must only contain digits.'
       
       if len(first_n) > 4 or len(second_n) > 4:
          return 'Error: Numbers cannot be more than four digits.'
    #===============================================================#

    ############################ Calculations #######################
    
    results = []

    for problem in problems:
        parts = problem.split()
        first_line.append(parts[0])
        operator_line.append(parts[1])
        second_line.append(parts[2])

        if parts[1] == '+':
           results.append(int(parts[0]) + int(parts[2]))
        else:
            results.append(int(parts[0]) - int(parts[2]))
    #===============================================================#

    ########################## Data output ##########################

    boxes = []
    message = ''
    i = 0

    # first line output
    while i < len(problems):
        width = 0
        spaces = 6
        if len(first_line[i]) > len(second_line[i]):
           width = 2 + len(first_line[i])
        else:
           width = 2 + len(second_line[i])

        boxes.append(width)
        message += ' ' * (boxes[i] - len(first_line[i])) + first_line[i]
        if i < len(problems) - 1:
            message += ' ' * 4

        i += 1
    message += '\n'

    # second line output
    i = 0
    while i < len(problems):
       message += operator_line[i] + ' ' * (boxes[i] - 1 - len(second_line[i])) + second_line[i]
       if i < len(problems) - 1:
            message += ' ' * 4
       i += 1
    message += '\n'

    # dash line output
    i = 0
    while i < len(problems):
       message += '-' * boxes[i]
       if i < len(problems) - 1:
            message += ' ' * 4
       i += 1
    #===============================================================#

    if not show_answers:
       return message
    else:
       message += '\n'
       i = 0
       while i < len(problems):
          message += ' ' * (boxes[i] - len(str(results[i]))) + str(results[i])
          if i < len(problems) - 1:
            message += ' ' * 4
          i += 1
    return message

print(f'\n{arithmetic_arranger(["32 - 698", "1 - 3801", "45 + 43", "123 + 49", "988 + 40"], True)}')
```

---
### ⇄ Saistības
Avots >>> [[šablons]]
Iepriekšēja lapa >>> [[šablons]]
Nākama lapa >>> [[šablons]]
___