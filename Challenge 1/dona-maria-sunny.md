##### Challenge 1: Am I prime or not?
##### Problem Statement: Implement a pure function which takes a natural number as an input and returns logical true if the said number is a prime number and logical false otherwise.
##### Author: Dona Maria Sunny (S6, CSE)

# Code
```python
def is_prime(number):
    if(number<=0):
        return("Invalid input! Enter a natural number.")
    elif(number==1):
        return("1 is neither a prime nor a composite number.")
    else:
        for i in range(2, (number//2)+1):
            if(number%i == 0):
                return(False)
        return(True)            

number=int(input("Prime Number Checker.\n Enter natural number to be checked?"))
print(is_prime(number))
```
# Explanation
Prime number is a number that is divisible only by itself and 1.
1. User enters the ```number``` to be checked, for prime or not.
2. Entered ```number``` is passed to the function and now the function **is_prime** is called.
3. Inside the function **is_prime** the following happens :
   * If the entered ```number``` is less than or equal to 0 then **Invalid input! Enter a natural number** is the output.
   * If the entered ```number``` is 1 then **1 is neither a prime nor a composite number** is the output.
   * If the entered ```number``` is 2 or greater than 2 then that ```number``` is divided by numbers ranging from 2 to ```number```//2. 
   
     If the ```number``` when divided by any numbers in the range, the remainder is equal to zero then **logical false** is the output. 
     Else, if the loop is exited not returning **logical false** then **logical true** is given as the output.
