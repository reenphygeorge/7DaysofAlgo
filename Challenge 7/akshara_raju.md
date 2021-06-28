# Code
```
#Python Code
#Problem Statement : Write a pure function that take two numbers as an input and finds the 
        #i. largest number that completely divides both numbers.
        #2. the smallest number that is the product of both numbers.

#Author : Akshara Raju
def gcd(number_1,number_2):
    if number_1 == 0:
        return(number_2)
    else:
        return gcd(number_2 % number_1, number_1)
def lcm(number_1,number_2):
      product = number_1 * number_2
      return(product//gcd(number_1, number_2))          


number_1 = int(input("First Number: "))
number_2 = int(input("Second Number: "))
print("largest number that completely divides both numbers : ", gcd(number_1,number_2))
print("smallest number that is the product of both numbers : ", lcm(number_1,number_2))

```
# Explanation
The 2 numbers are assigned to **number_1** and **number_2**. These numbers are passed as arguments to functions **gcd()** and
lcm(). The gcd() returns the largest number that completely divides both numbers and lcm() returns the 
the smallest number that is the product of both numbers. \
**OUTPUT** \
First Number: 27\
Second Number: 36\
largest number that completely divides both numbers :  9\
smallest number that is the product of both numbers :  108





          


     


