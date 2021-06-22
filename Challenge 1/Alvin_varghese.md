CODE
======
```C
/**************************************************************************
* File           :  Experiment 1                                                    
* Description    :  C program to return logic value by checking prime                                    
* Author         :  Alvin varghese                                              
* Version        :  1.0
* Date           :  22/06/2021                                                
****************************************************************************/
#include<stdio.h>
int check_prime(int);
 int main()
{
   int number, result;
   printf("Enter the number to check if it is prime or not.\n");
   scanf("%d",&number);
   result = check_prime(number);
   if ( result == 1 )
      printf("TRUE");
   else
      printf("FALSE");
   return 0;
}
int check_prime(int n)
{
   int i;
   for ( i = 2 ; i <= n- 1 ; i++ )
   { 
      if ( n%i== 0 )
     return 0;
   }
    return 1;
}
```
EXPLANATION
======
- We have created a function - check_prime() ,that accepts value from the main().    
  
- Inside the function check_prime(),the logic for checking prime number is implemented in which i is a loop variable that  iterates from 2 to the (number-1). 

- If number is divisible by any of the value of i,then it returns 0  else it returns 1.  

- 0 indicates the logical FALSE and 1 indicates the logical True.  

- Therefore it returns 0 if it is not a prime number and returns 1 if it is a prime number.  

- In the main() ,the user is asked   to enter  the number to check for the prime and which is sent to the check_prime() function.  

- When the return value from the check_prime() is passed to the main(),it check for the return and print the respective logical value of 1 or 0.  
