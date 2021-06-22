
```python

def prime_checker(number):                              
    result = 1
    for temp_var in range(2, (number//2)+1):    
        if number % temp_var == 0:
            result = 0                          
            break
    if result == 0:
        print(bool(result))                     
    else:
        print(bool(result))

        
number = int(input("Enter any natural number: "))
prime_checker(number)
```




## Explanation

1. A function named 'prime_checker()' is defined. It contains: 
    *  A variable 'result' assigned with value 1 (returns True when accessed with bool function).
    *  A loop that checks the divisibilty of the passed arguement by numbers ranging from 2 to half of the passed argument.
    *  A print statement that returns the boolean value of 'result'.

2. When any value in the specified range divides the passed arguement perfectly:
    *  The value of 'result' is modified as 0 (return False when accessed with bool function).
    *  Control is taken out of loop.

3. When 'prime_checker()' is called it will analyse value in 'result' and return its boolean value.
