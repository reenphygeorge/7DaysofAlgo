# code
```python
def is_prime(n):
    flag=True
    if (n > 1):
        for i in range(2,n):
            if (n % i == 0):
                 flag=False
                 break
           
    if (flag ==False):
        return flag
    else:
        return flag
n=int(input())
print (is_prime(n))
```
# Explanation
Prime Numbers are those numbers which have 1 and itself only as their factors.No other numbers can divide it.Only natural numbers can be prime numbers.so weare using the first if loop where it checks if number is greater than 1.We have declared a variable flag and if any number can divide our input,flag value is set False which means it is not a prime number.If flag is true,It is a prime number and if flag is False,its not a prime number.

