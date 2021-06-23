# Challenge 2

## Code: Python3

```python
# word repesentation of numbers between 0 and 999.
def spell_it(num):
    dict_ref= {
        0:" ",
        1:"one",
        2:"two",
        3:"three",
        4:"four",
        5:"five",
        6:"six",
        7:"seven",
        8:"eight",
        9:"nine",
        10:"ten",
        11:"eleven",
        12:"twelve",
        13:"thirteen",
        14:"fourteen",
        15:"fifteen",
        16:"sixteen",         
        17:"seventeen",         
        18:"eightteen",      
        19:"nineteen",       
        20:"twenty",
        30:"thirty",
        40:"forty",
        50:"fifty",
        60:"sixty",
        70:"seventy",
        80:"eighty",
        90:"ninety"
    }
   
    print(dict_ref[num],end=' ')
        
n=str(input())
if int(n)==0:
    print('zero')
else:    
    numbers=list(map(int,list(n)))
    if len(numbers)==1:
        spell_it(numbers[-1])
    if len(numbers)==2:
        if numbers[-2]*10 + numbers[-1]<20:
            spell_it(numbers[-2]*10 + numbers[-1])
        else:
            spell_it(numbers[-2]*10)
            spell_it(numbers[-1])
    if len(numbers)==3:
        spell_it(numbers[-3]),print("hundred",end=' ')
        if numbers[-2]*10 + numbers[-1]<20:
            spell_it(numbers[-2]*10 + numbers[-1])
        else:
            spell_it(numbers[-2]*10)
            spell_it(numbers[-1])
```

## Code Explanation
* The function `spell_it()` is declared and input from the user(any number between 0 and 999) is passed to the function
* A dictionary `dict_ref` is used to store some selected numbers and its corresponding word representation as key-value pairs that is inevitable for spelling the numbers between 0 and 999
* If the input number is 0, then "zero" is displayed 
* The input number is split as digits and length of the input number is found using `len()`
  * Depending on the length of the input number, mathethematical operations are performed on digits based on its position and 
    the function `spell_it()` is recursively called and accordingly, numbers are mapped to the word representation of the numbers in `dict_ref`

 
 ## Output
 number| number in words          |
---    | ---                      |
 | 6   |six                       |
 | 15  |fifteen                   | 
 | 102 |one hundred two           |
 | 123 |one hundred twenty three  |
 | 456 |four hundred fifty six    |


---
 Done with ☕️ and code 🙋‍♀️
