# Code
```
def isPrime(num):
    if num > 1:
        for i in range(2, int(num/2)+1):
            if num % i == 0:
                return False
        return True
    else:
        return False


print(isPrime(17))
```

# Explanation
A positive integer greater than 1 which has no other factors except 1 and the number itself is called a Prime number.  
The program proceed if the number is greater than 1 or return logical False.  
We check if 'num' is divisible by any number from **2 to half of the given number.**  
If we find any number that divides, we return logical False.  
If we did not find any number which divides 'num' then the number is Prime and we will return logical True.

Implemented a **Pure function** which returns   
> **logical True** for prime numbers   
> **logical False** for composite and negative numbers  

******************************
Language used: Python3
