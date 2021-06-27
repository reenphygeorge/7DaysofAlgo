# Code
```python 3.8
def gcd(a,b):
    if(b==0):
        return a
    else:
        return gcd(b,a%b)
def lcm(a,b):
    return(b/gcd(a,b))*a
a=int(input("Enter the first number:"))
b=int(input("Enter the second number:"))
print("The largest number:",+gcd(a,b))
print("The smallest number:",+lcm(a,b))
print("The product of both numbers:",+(gcd(a,b)*lcm(a,b)))
```

# Explanation
- Enter the numbers.
- find the largest number :
   - if second number=0
      - return first number
   - else:
      - return largest number
- find the smallest number:
    - by dividing b with gcd and then multiply with a
- find the product by multiplying lcm with gcd
