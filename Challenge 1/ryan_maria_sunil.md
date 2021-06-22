# Code
```
def is_prime(n):
  if n<1:
    return""
  elif n==1:
    return False
  elif n==2:
    return True
  else:
    for i in range(2,n//2+1):
      if n%i==0:
        return False
    return True

print(is_prime(7))
```

# Explanation
Here is_prime is a user defined function which accepts the number to be checked for prime.
In this function,we first check whether the given number is a natural number by checking whether the given no is below 1. If so the function will return a empty string. Then the function checks whether the given no is 1 .If the no is 1 then the function returns False.  Then the function checks whether the given no is 2 .If the no is 2 then the function returns True. If the no is above 2 then we implement a loop from 2 to the no/2. If any of the no in the loop divides the given no leaving a remainder 0 then the function returns False. Ifthe no is prime after then the loop will run till the end without a break and will return True.

