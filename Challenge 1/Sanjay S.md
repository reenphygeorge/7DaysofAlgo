# Code
```
def is_prime(number):

    if number < 0 or number-int(number) != 0:
        return str(number)+" is not a Whole number"

    if number in [0, 1]:
        return str(number)+" Neither Prime nor Composite"

    else:
        for i in range(2, (number//2) + 1):
            if number % i == 0:
                return str(number) + " is a Composite number"
        return str(number) + " is a Prime number"


print(is_prime(7))

```

# Explanation
To check whether the given number is a prime number, we need to check several cases. These are:

1. **Check whether input is a whole number**
    For a number to qualify as a whole number, the number shouldn't be a negative integer nor a fraction.
    
    * ```number < 0``` checks whether the number is negative; _numbers less than 0 are negative._
    * ```number-int(number) != 0``` checks whether the number is fractional. int() converts the number to an integer, and then the difference is found. _If the difference is not 0, the number is a fraction._

2. **Check whether the number is 0 or 1**
   _0 and 1 is considered as neither prime not composite_
   So ```number in [0, 1]``` is used to verify the same.

3. **Check whether the number is divisble by any number other than  one or itself**

    To execute this, we divide the number, say x by the numbers in the range 0 to (x/2), and if for any of these cases, if the remainder is 0, the number is a composite number and the function returns.
    
    Incase the given number passes the for loop without returning, the number is prime and the function returns "Prime".




