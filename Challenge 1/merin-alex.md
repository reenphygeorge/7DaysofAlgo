# Challenge 1
## Code: Python3

```python
def is_prime(number):    
    isprime=True
    
    if number>1:
        for i in range(2,number//2+1):
            if number%i==0:
                isprime=False
                return isprime
        return isprime
    
    else:
        isprime=False
        return isprime
    
number=int(input())
print(is_prime(number))

```
## Code Explanation

The function definition `is_prime` accepts an integer called `number` as argument and 
a boolean variable `isprime` is declared to be `True` within the function body.
 
1. if input number is greater than 1, then for values in the `range(2 to number//2+1)`, check if the number is completely divisible by any value in that range, 
if so return `isprime` as `False`.
  
   * The range has been chosen between `2 and number//2+1` because
   all the factors of a number excluding that number, lies in the range 1 and half of that number,  so we need to iterate the loop till half of that number
   and hence this range has been chosen for checking prime condition and thus reducing the number of iterations and hence saving time.
      
2. If during the iteration process, if none of the values divide the number completely, return `isprime` as `True`.
3. For all other cases, return `isprime` as `False`

## Output

| number        | isprime       | 
| ------------- |:-------------:| 
| 2             | True          | 
| 4             | False         |   
| 7             | True          |   

___
Done with ☕️ and code 🙋‍♀️

