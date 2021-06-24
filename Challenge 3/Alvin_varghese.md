CODE
====
```C
/***********************************************************************************************
* File           :  Experiment 1                                                    
* Description    :  C program to orint the hexadecimal equivalent of decimal and binary number                                    
* Author         :  Alvin varghese                                              
* Version        :  1.0
* Date           :  24/06/2021                                                
***********************************************************************************************/
#include <stdio.h>
int binarytohexa(int number);
int decimaltohexa(int number);
int main()
{   int choice,num;
    printf("1.BINARY TI HEXA\n2.DECIMAL TO HEXA\n");
    scanf("%d",&choice);
    switch (choice)
    {
    case 1: printf("enter the binary number : ");
            scanf("%d",&num);
            binarytohexa(num);
        break;
    case 2 : printf("enter the decimal number :");
            scanf("%d",&num);
            decimaltohexa(num);
        break;
    default:printf("wrong choice");
        break;
    }
    return 0;
}
int binarytohexa(int number)
{
    long int  hexadecimalval = 0, i = 1, remainder;
    while (number != 0)
    {
        remainder = number % 10;
        hexadecimalval = hexadecimalval + remainder * i;
        i = i * 2;
        number = number / 10;
    }
    printf("EQUIVALENT HEXADECIMAL IS : %lX", hexadecimalval);
    return 0;
}
int decimaltohexa(int number)
{
      long  remainder;
    int i, j = 0;
    char hexadecimalnum[100];
    
 
    while (number != 0)
    {
        remainder = number % 16;
        if (remainder < 10)
            hexadecimalnum[j++] = 48 + remainder;
        else
            hexadecimalnum[j++] = 55 + remainder;
        number= number / 16;
    }
 
    printf("THE HEXADECIMAL EQUIVALENT IS : ");
    for (i = j; i >= 0; i--)
            printf("%c", hexadecimalnum[i]);
    return 0;
}

```
EXPLANATION
===========
- Two functions-`decimaltohexa()` and `binarytohexa()` is created to calculate and display the hexadecimal of respective numbers.  
- Inside `main()` option to choose between decimal to hexa and binary to hexa is given to the user.  
- Number entered by the user is passed to the respective function.  
- Int the function-`binarytohexa()`,the hexadecimal of the binary number is found by taking each digit and returning the respective hexadecimal number.  
- In the function-`decimaltohexa()`,the number entered is taken as each digit and the reminder with 16 is stored in another variable.  
- The cOndition checks if the remainder is greater than 10 and if so,it returns the specific character in hexadecimal(A-F) and each digit of hexadecimal is printed as a character.
