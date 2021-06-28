# code
```python
def number(num1,num2):

    smallest=min(num1,num2)
    largest=max(num1,num2)
    if(smallest ==0):
        print ("The Largest number that divide both numbers is:",largest)
        print("The smallest number that form product of both number is:",smallest)
    elif (largest % smallest == 0):
        print ("The Largest number that divide both numbers is:",smallest)
        print("The smallest number that form product of both number is:",largest)
    else:
        for i in range(smallest,0,-1):
            if (smallest % i==0 and largest % i==0):
                print ("The Largest number that divide both numbers are:",i)
                print("The smallest number that form product of both number is:",largest*smallest)
                break
        
num1,num2=map(int,input("Enter 2 numbers seperated by space\n").split())
number(num1,num2)
```
# Explanation
In function number,we give two parameters,num1 and num2.smallest of both number is assigned to variable smallest and largest is assigned to variable largest.The largest number that divide both numbers
can be the smaller number among them(variable-smallest) or less than smallest.So we decrement smallest value by one and try to divide it by both number.That divisible number will be largest number that can divide bith.

