# Code
```
"""
Created on Wed Jun 23 11:59:57 2021

@author: Carol Varghese

Function to find if a number is prime or not

"""

        def is_prime(number):                               #Function Definition
            
            if(number<=1)                                   #checking if number is lessthan or equal to 1
            
                if(number==1)                               #checking if the number is 1
                
                    return False                            #exiting function as 1 is not a prime number
                
            else:
                
                return                                      #exiting function it's an invalid input
            
            for i in range(2,int(number/2)):                #for loop in the range 2 to half of the number
                                                            #type conversion used for obtaining natural number 
                                                            
                if(number%i==0):                            #conditional statement to find if it has any factors 
                                                            #other than 1 and itself              
                                                            
                   return False                             #printing false as it is not a prime number
                                                            #and Exiting the function 
                
                                            
            return True                                     #printing true as it is a prime number
                                                            #Exit function
        
        
```

# Explanation
Problem statement: Construct a function to find if a number is prime or not 
and print true if it is a prime number or print false if it is not a prime number

Working of function

 checks weather the number is less than 2  
   if it is less than 2 then it checks if it is 1  
     if it is 1 then it will return false since it is not a prime number   
     if not then the number will be 0 or negative hence the function returns an empty string  
   if it is greater than 2 then it enters a for loop  
        where the number is continuously divided by numbers ranging from 2 to half of the number and the reminder analysed   
        if the remainder equals to zero then it returns false since the number ha another factor other than 1 and itself  
       if the for loop end without any returns the function continues   
       and return true since there are no factors other than 1 or itself for that number   
       hence it is a prime number. 
