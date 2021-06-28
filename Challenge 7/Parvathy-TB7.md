# Code
```python
def gcd(a,b):
   while(b):
       a,b=b,a%b
   return a
def lcm(a,b):
   l=(a*b)//gcd(a,b)
   print(l)
n1=int(input("First number:"))
n2=int(input("Second number:")) 
print(gcd(n1,n2))
lcm(n1,n2)
```
# Explanation
1. Input 2 numbers(n1 and n2)
2. To find the largest number that completely divides both numbers,that is GCD call `gcd()` function
   * Inside the function contains a loop while the value of `b`(second number) is non-zero
   * At each iteration value of `a` changed to `b`, and `b` changed to `a%b`
   * Once the loop stop iteration `a` will contain GCD
   * Return `a`
3. To find the smallest number that is the product of both numbers, that is LCM call `lcm()` function
   * Inside the function mulitiply the two numbers then floor divide the result with the return value from `gcd()` after calling
   * Then print the result
