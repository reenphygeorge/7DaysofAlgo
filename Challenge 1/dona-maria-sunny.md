##### Challenge 1: Am I prime or not?
##### Problem Statement: Implement a pure function which takes a natural number as an input and returns logical true if the said number is a prime number and logical false otherwise.

# Code
```python
def is_prime(number):
    flag=0
    if(number<=0):
        return("Invalid input! Enter a natural number.")
    elif(number==1):
        return("1 is neither a prime nor a composite number.")
    elif(number==2):
        return(True)
    else:
        for i in range(2, number):
            if(number%i == 0):
                return(False)
            else:
                flag=1
        if(flag==1):
            return(True)            

number=int(input("Prime Number Checker.\n Enter natural number to be checked?"))
print(is_prime(number))
```
# Explanation
Prime number is a number that is divisible only by itself and 1.
1. User enters the number to be checked, for prime or not.
2. Entered value is passes to the function and now the function **is_prime** is called.
3. Inside the function **is_prime** _flag_ value is set to 0 and the following happens :
   * If the entered number is negative or less than 0 then **Invalid input! Enter a natural number** is the output.
   * If the entered number is 1 then **1 is neither a prime nor a composite number** is the output.
   * If the entered number is 2 then **logical true** is the output.
   * If the entered number is greater than 2 then that ```number``` is divided by numbers ranging from 2 to one less than the ```number```. 
   
     If the ```number``` is divisible by any numbers in the range then **logical false** is the output. Else, if the ```number``` is not divisible _flag_ value is set to          1 and **logical true** is given as the output.
