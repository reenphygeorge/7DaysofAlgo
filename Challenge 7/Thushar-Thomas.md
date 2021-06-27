# Code
```python
'''
Documentation
Program to take two numbers from user and return
1. The Largest number that completely divides both numbers
2. The Smallest number that is the product of both numbers

Name   : Thushar Thomas
Branch : AI & DS
'''
def small_lar(a,b):    # Calls a function to find multiple and factor
    fact1=[]
    fact2=[]
    if a==b:    # If both numbers are equal
        print("\nBoth numbers are equal. \nTherefore",a,"is the largest number that completely divides both numbers.")
        print(b,"the smallest number that is the product of both numbers.")
        return
    if a==0 or b==0:    # If one of the number is zero
        print("'0' is not a factor or multiple of any number")
        return
    if a%b==0 or b%a==0:    # If one of the number is the factor of other
        if a>b:
            print(b,"is the largest number that completely divides both numbers. ")
            print(a,"the smallest number that is the product of both numbers. ")
        else:
            print(a,"is the largest number that completely divides both numbers. ")
            print(b,"is the smallest number that is the product of both numbers. ")
    else:
        for i in range(1,a+1):
            if a%i==0:
                fact1.append(i)
        for i in range(1,b+1):
            if b%i==0:
                fact2.append(i) 
        if len(fact1)==2 or len(fact2)==2:    # If one of the number is prime
            print("1 is the only number that completely divides both numbers. ")
            print(a*b,"the smallest number that is the product of both numbers. ")
        else:
            for i in range(len(fact1)):
                for j in range(len(fact2)):
                    if fact2[j]%fact1[i]==0:
                        lar=fact1[i]
            sml=int((a*b)/lar)
            print(lar,"is the largest number that completely divides both numbers. ")
            print(sml,"the smallest number that is the product of both numbers. ")
num1=int(input("Enter the first number: "))
num2=int(input("Enter the second number: "))
small_lar(num1,num2)    # Calling the function
```

# Explanation
#### In this program, user can enter two values and get it's factor and multiple.
<p> <br/>This program does the following
          * **If both numbers are equal:** It returns the number itself as it's factor and multiple.
          * **If one of the number is zero:** Returns '0' is not a factor or multiple of any number.
          * **If one or both number is prime:** Returns '1' as the largest factor and the product of the two numbers as multiple.
          * **If non of the above:** The program uses 'for' loop to find it's largest factor and "product/factor" as the multiple.
<br/>Thank you

