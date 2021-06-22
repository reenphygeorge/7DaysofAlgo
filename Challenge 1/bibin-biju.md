# CODE

```c
#include<stdio.h>

#include<stdbool.h>

bool primeChecker(int number);

int main()
{

    int number;
    printf("\nEnter any positive number to check whether it's prime or not: ");
    scanf("%d",&number);
     if((number==0) || (number==1))

        {
            printf("Neither prime nor composite.");
            
        }
   else
    if (primeChecker(number))

     printf("%d is a prime number.",number);
    else  
    printf("%d is not a prime number.",number);
    return 0;
}

bool primeChecker(int number)

{

    int i;
    bool condition = true;
    for(i=2;i<=(number/2);i++)
    {
        if(number%i==0)
        {
            condition=false;
            return condition;
            break;
        }
       
    } 
    return true; 
}
```

# EXPLANATION
We are able to check whether a number is a prime number or not unless it's a positive number. So the first prime number starts from 2 and goes on. If one enters 0 or 1, I've used a simple if condition out of the function definition as it's much easier. I've used the boolean conditions using <stdbool.h> header file and defined the user defined function, "primeChecker" out of main function by using function prototype ahead of main function.
Here I used the variable "condition' as the boolean and initially set it to true.

When the for loop executes, it is actually showing as boolean false. Hence the value is printed as prime or not in the printf statement in the main function.
