# Code
```python3
def gcd(a, b):
    if a == 0:
        return b
    else:
        return gcd(b % a, a)


def lcm(a, b):
    prod = a * b
    hcf = gcd(a, b)
    return prod // hcf

print("Enter the numbers seperated by space")
a, b = map(int, input().split())
hcf,lcm=gcd(a,b),lcm(a,b)
print("The largest number that completely divides both numbers is {}".format(hcf))
print("The smallest number that forms the product of both numbers is {}".format(lcm))
print("The product of both numbers={}".format(hcf*lcm))


```

# Explanation
We need to write a program  that finds
1. largest number that completely divides both numbers.
2. the smallest number that is the product of both numbers.
* For this, we ask the user  to input two numbers seperated by space
* The largest number that completely divides both numbers is the hcf of that numbers.We implement a function hcf and pass the user input as arguments
*  * If the value of first argument=0,we return the second argument.Else we recursively call the function passing the remainder of second argument divided by first argument and first argument as its parameters.Finally the hcf is returned
*  The smallest number that form the product of both numbers is its LCM,we implement a function for this.
*  * We know the product of two numbers is equal to product of hcf and lcm,so we call the gcd() function and divide the orginal product with the hcf returned from gcd() and return it as lcm.
*  We print the highest common factor ,least common multiple and orginal product.

# OUTPUT
Enter the numbers seperated by space
26 91
The largest number that completely divides both numbers is 13
The smallest number that forms the product of both numbers is 182
The product of both numbers=2366

