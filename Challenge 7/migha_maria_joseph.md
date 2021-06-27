# Code
```python
def calculate_gcd(x, y):
   while(y):
       x, y = y, x % y
   return x
def calculate_lcm(x, y):
   lcm = (x*y)//calculate_gcd(x,y)
   return lcm
num1 = int(input("num1:"))
num2 = int(input("num2:")) 
print("The G.C.D is", calculate_gcd(num1, num2))
print("The L.C.M. is", calculate_lcm(num1, num2))
```
# Explanation
*  Write a pure function that take two numbers as an input and finds the
   *   largest number that completely divides both numbers.ie GCD(Greatest Common divisor)
   *   the smallest number that is the product of both numbers.ie LCM(Least Common Multiple)
* GCD  is defined as the greatest positive number,which is a common factor of both the positive integers (num1,num2) 
   *    here is to find the greatest number or divisor or factor that divides the given numbers evenly with the remainder zero
* LCM can be found by using GCD,as (num1*num2)//gcd(num1,num2) 
