___
**Datums:** 2025-07-28   
**Laiks:** 12:37 
❚ **Tagi:** #python 
⌬ **Kurss:**  `Python`

---
### ⬢ Detalizēts apraksts
#### Programma

```python
def square_root_bisection(square_target, tolerance=1e-7, max_iterations=100):
    if square_target < 0:
        raise ValueError('Square root of negative number is not defined in real numbers')
    if square_target == 1:
        root = 1
        print(f'The square root of {square_target} is 1')
    elif square_target == 0:
        root = 0
        print(f'The square root of {square_target} is 0')

    else:
        low = 0
        high = max(1, square_target)
        root = None
        
        for _ in range(max_iterations):
            mid = (low + high) / 2
            square_mid = mid**2

            if abs(square_mid - square_target) < tolerance:
                root = mid
                break

            elif square_mid < square_target:
                low = mid
            else:
                high = mid

        if root is None:
            print(f"Failed to converge within {max_iterations} iterations.")
    
        else:   
            print(f'The square root of {square_target} is approximately {root}')
    
    return root
```

---
### ⇄ Saistības
Avots >>> [freecodecamp.org/learn/scientific-computing-with-python/learn-the-bisection-method-by-finding-the-square-root-of-a-number/step-21](https://www.freecodecamp.org/learn/scientific-computing-with-python/learn-the-bisection-method-by-finding-the-square-root-of-a-number/step-21)
Iepriekšēja lapa >>> [[abs() metode]]
Nākama lapa >>> [[Navigācija - Python]]
___