# CODE
```Python
def gcd(num1,num2):
    if num1 == 0:
        return(num2)
    else:
        return gcd(num2 % num1, num1)
def lcm(num1,num2):
      product = num1 * num2
      return(product//gcd(num1, num2))          


num1 = int(input("Enter first number:\t"))
num2 = int(input("Enter second number:\t"))
print("Largest number that completely divides both numbers : ", gcd(num1,num2))
print("Smallest number that is the product of both numbers : ", lcm(num1,num2))
```

# EXPLANATION
  *The two numbers are taken from the user in the main function
  *For finding the largest number that completly divides both numbers ,the numbers are passed to the function gcd
  *Gcd is calculated by a recursive function
  *For finding the smallest number that is the product of both numbers, the numbers are passed to the function lcm
  *The lcm is calculated by multiplying the two numbers and then dividing that product with the gc obtained in the eariler function
