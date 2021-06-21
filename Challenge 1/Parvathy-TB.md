## Code
```
def is_prime(n):
    flag=1
    for i in range(2,n):
        if(n%i==0):
            flag=0
            break
    if(flag==0):
        print(bool(flag))
    else:
        print(bool(flag))
n=int(input("Enter a natural number:"))
is_prime(n)
```
## Explanation
Prime numbers are numbers that have only 2 factors: 1 and themselves.
The function `is_prime(n)` will check whether the number n is divisible by any of the numbers between 2 and (n-1), 
and if possible the function will print a `False`(which means n is not a prime number) and if not possible the function will print `True`(which means n is a prime number).
