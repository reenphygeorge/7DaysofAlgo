##### Challenge 7: Factors and Multiples.
##### Problem Statement: Write a pure function that take two numbers as an input and finds the, largest number that completely divides both numbers and the smallest number that is the product of both numbers.
##### Author: Dona Maria Sunny (S6, CSE)
##### Language used: Python 3
# Code
```python
def findHCF(number1, number2):
    if(number1==number2):
        return("You entered same numbers. Enter different numbers.")
    elif(number1==0 or number2==0):
        return("HCF and LCM is not defined.")
    else:
        if(number1>number2):
            smallestNumber=number2
        else:
            smallestNumber=number1
        while(smallestNumber>=1):
            if(number1%smallestNumber==0 and number2%smallestNumber==0 ):
                hcf=smallestNumber
                break
            smallestNumber=smallestNumber-1
        lcm=(number1*number2)//hcf
        return("\nOUTPUT:\n HCF of {} and {} is {}.\n LCM of {} and {} is {}.".format(number1,number2,hcf,number1, number2, lcm))


print("Factors and Multiples.(HCF and LCM of two numbers)")
number1=int(input(" Enter first number:"))
number2=int(input(" Enter second number:"))
print(findHCF(number1, number2))

```
# Explanation
1. User enters ```number1``` and ```number2```. 
2. Now the function **findHCF()** is called. ```number1``` and ```number2``` are passed to it.
3. Inside the function the following happens:
   * If both ```number1``` and ```number2``` are same, then ***You entered same numbers. Enter different numbers*** statement is returned.
   * Else if ```number1``` or ```number2``` is 0, then ***HCF and LCM is not defined*** statement is returned.
   * Else, smallest among ```number1``` and ```number2``` is found. 
     
     Using ***%*** operator largest number that completely divides both numbers(HCF) is found.
     
     Now using the equation, ***HCF(number1, number2) × LCM(number1, number2) = number1 × number2***, the smallest number that is the product of both numbers(LCM) is found.
     
     HCF and LCM of both the numbers are returned.
