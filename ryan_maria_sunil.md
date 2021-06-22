# Code
```
from sympy import isprime

def is_prime(n):
  if n>=1:
    return(isprime(n))
  return("")

print(is_prime(7))
```

# Explanation
Here is_prime is a user defined function which accepts the number to be checked for prime.
In this function,we first check whether the given number is a natural number.
If it is a natural number, we return the result of the library function isprime which is contained in sympy module.
isprime is a function to check whether the given number is prime or not. The result of the function isprime is True if the given number is prime and False if not.
If the given number is not a natural number then an empty string is returned.
