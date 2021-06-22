# Code

```
def isPrime(num):
        isNumPrime = True
        for i in range (2, int(num/2) + 1):
            if num%i == 0:
                isNumPrime = False
                break
        return isNumPrime

print(str(isPrime(17)))
```

# Explanation

We can check whether a no. is prime or not by checking if the given no. divided by any no. less than the given no. (except 1) yields a remainder of 0. If it does, then the no. is composite, else it's prime.

Initially, the `isPrime` flag is set to True

The program loops through the range 2 to half of the given no. (because no.s greater than half of any given no. will never produce a remainder when divided by the original number. This reduces the time complexity by half 🌚). If at any point the given number divided by the loop variable yields a result of 0, the `isPrime` flag is set to false and the loop execution is terminated. Finally, the boolean value of `isPrime` is returned to the caller function.
