# Code
```python
def hcf_and_lcm(x,y):
    no1,no2=x,y
    while(y):
        x, y = y, x%y
    hcf=x
    if hcf==0.0:
        return hcf,0.0
    lcm=(no1*no2)// hcf
    return hcf,lcm

x=float(input("Enter 1st no : "))
y=float(input("Enter 2nd no : "))
hcf,lcm=hcf_and_lcm(x,y)
print("Largest number that completely divides "+str(x)+" and "+str(y)+" is "+str(hcf))
print("The smallest number that is the product of "+str(x)+" and "+str(y)+" is "+str(lcm))
```

# Explanation
The two numbers are taken as input from user. These numbers are passed to the function hcf_and_lcm. In the function, the while loop is used to find the hcf value. In the loop we divide 
the greater by smaller and take the remainder.Then, divide the smaller by this remainder. This is repeated until the remainder is 0. After the loop the x value gives the hcf.
If the hcf is 0 ,then return the hcf and a 0 value. If hcf is not 0,then calculate the product of two numbers and divide the product by hcf value obtained and assign the result to lcm. 
At the end of the function, return hcf and lcm. Now print the results.
