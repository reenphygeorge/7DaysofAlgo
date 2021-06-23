CODE
====
```C
/**************************************************************************
* File           :  Experiment 1                                                    
* Description    :  C program to print numbers in words                                    
* Author         :  Alvin varghese                                              
* Version        :  1.0
* Date           :  23/06/2021                                                
****************************************************************************/
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
void spellit(char *number) {
   int length = strlen(number);
   if (length > 4) {
      printf("PLEASE ENTER A NUMBER LESS THAN 100000\n");
      return;
   }
   char *single_digit[] = { "zero", "one", "two", "three", "four","five", "six", "seven", "eight", "nine"};
      char *tens_place[] = {"", "ten", "eleven", "twelve", "thirteen", "fourteen", "fifteen", "sixteen", "seventeen", "eighteen", "nineteen"};
      char *tens_multiple[] = {"", "", "twenty", "thirty", "forty", "fifty","sixty", "seventy", "eighty", "ninety"};
      char *tens_power[] = {"hundred", "thousand"};
   if (length == 1) {
      printf("%s\n", single_digit[*number - '0']);
      return;
   }
   while (*number != '\0') {
      if (length >= 3) {
         if (*number -'0' != 0) {
            printf("%s ", single_digit[*number - '0']);
            printf("%s ", tens_power[length-3]); 
         }
         --length;
      }
      else {
         if (*number == '1') {
            int sum = *number - '0' + *(number + 1)- '0';
            printf("%s\n", tens_place[sum]);
            return;
         }
         else {
            int i = *number - '0';
            printf("%s ", i? tens_multiple[i]: "");
            ++number;
            if (*number != '0')
               printf("%s ", single_digit[*number - '0']);
         }
      }
      ++number;
   }
}
int main() {
    char number[5];
   printf("enter the number : ");
   scanf("%s",&number);
   spellit(number);
   return 0;
}
```
EXPLANATION
===========
- the number to be converted to words is accepted in the `main()` and is passed as a pointer to the function `spellit()`.  
- in `spellit()` the number entered is converted to string and the length is calculated. and the checks if the number is less than 4 digits.  
- The words for different digits are stored in differenr pointer variables.  
- next the main conditions starts - first it checks if the number is a single digit and prints the respective word for the number by pointer adress.  
- next `*number -'0'` gives the numeric digit of the pointer and if it is not equal to 0 ,it gives the respective hundreds and thousands place.  
- `sum = *number - '0' + *(number + 1)- '0'` gives the tenth place,if the number is starting with 1 and is less than 20 (for number 1-19)
- now the function `spellit()` is called in `main()`.
