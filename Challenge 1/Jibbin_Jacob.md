# CODE
/**************************************************************
 * File             : PrimeorNot
 * Description      : C Program to check whether the entered number is prime or not.
 * Author           : Jibbin Jacob
 * Date             : 21/06/2021
 * ************************************************************/

```c

#include<stdio.h>

#include<stdbool.h>

int isPrime(int number)

    {

    int i;
    _Bool result=1;
    for(i=2;i<=(number/2);i++)
    {
        if(number%i==0)
        {
            result=0;
            break;
        }  
    }
    if(number==1)
    {
        printf("The entered number %d is neither prime nor composite.",number);
    }
    else
    {
        printf("%d",result);   
    } 
}

int main()

{

    int number;
    printf("Enter a natural number:");
    scanf("%d",&number);
    isPrime(number);
    return 0;
}

```

# EXPLANATION

* Prime numbers are the numbers which are divisible by itself and 1.
* In this program the user is asked to enter a natural number.
* Then the function isPrime() is called.
* At the beginning of the function the boolean is defined as result=1.
* To use bool a header file have to be given. The header file used is stdbool.h
* In boolean condition 
        0 means False
        1 means True.
* Then the complier checks for the condition.
* A for-loop is provided for executing the programing till the condition. In the program a variable 'i' is given to run the program till the half of the number.
* Following that, if conditions are given.
* If the number has a remainder 0, then the number is not a prime number. So the output shown will be 0.
* If the value of i is greater than the half of the number, then the number is a prime number. And the output shown will be 1.
* If the number entered is 1, then the output will be neither a prime nor composite.



