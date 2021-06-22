# Code
```
from math import sqrt
def is_prime(n):
    prime = [True] * (n + 1)
    prime[0] = False
    prime[1] = False
    for i in range(2, int(sqrt(n)) + 1):
        if prime[i] == True:
            for j in range(i * i, n + 1, i):
                prime[j] = False
    length=len(prime)
    if prime[length-1]==True:
        return True
    else:
        return False


print(is_prime(7))
```

# Explanation
Let n be the number to be checked.This problem statement is executed here utilizing the Sieve of Eratosthenes algorithm. First a boolean list of length, (n+1) (since we are  updating for all numbers from 0 to n ) is created to store whether the numbers are prime or not and very item in the list is initialized with a 'True' value.The items at index 0 and 1 are set false since the lowest prime number is 2.For all numbers from 2 to squareroot(n)+1 ,we check whether the value of corresponding item  in the prime list is true or not .If it is True ,we update the list item of all numbers  greater than equal to square of that number and are divisible by that number(both conditions must be satisfied) to 'False'.After completing this loop,we have in our prime list ,a 'True' value corresponding to all prime numbers and a 'False' value corresponding to all non primes.The list item at the last index is our required output.

