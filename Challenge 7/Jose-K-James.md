# Code
```
#include <stdio.h>
int gcd(int x, int y);

int main()
{
    int num1, num2, hcf, lcm;

    printf("Enter two integer Values:\n");
    scanf("%d %d", &num1, &num2);

    hcf = gcd(num1, num2);
    printf("largest number that completely divides both numbers (HCF):\n%d", hcf);
    printf("\nSmallest number that is the product of both numbers (LCM):\n%d", (num1 * num2) / hcf);
    return 0;
}

int gcd(int x, int y) //recursive function
{
    if (y == 0) //recursion termination condition
    {
        return x;
    }
    else
    {
        return gcd(y, x % y);
    }
}
```

# Explanation
GCD is the greatest positive integer that divides the two integers. LCM is the smallest number that is divisible by both integer.   
- In this program, **recursive function** 'gcd' returns the value of gcd.  
- The termination condition of the recursive function is 'y == 0' which checks whether the number is equal to zero or not.  

Implemented a **Pure Function** that  returns  
> largest number that completely divides both numbers **(HCF)**.   
> Smallest number that is the product of both numbers **(LCM)**.  
******************************
Language used: C   
