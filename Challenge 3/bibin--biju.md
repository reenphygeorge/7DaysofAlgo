Code
===
```c
#include<stdio.h>
int dectohexa(int number)
{
   int i=0,j=0,remainder=0;
   char hexaDec[150];
   while(number>0)
   {
     
      remainder=number%16;
      if(remainder<10)
      {
        hexaDec[i]=remainder+48;
        i++;
      }
      else
      {
          hexaDec[i]=55+remainder;
          i++;
      }
      number=number/16;
   }
   for(j=i-1;j>=0;j--)
   {
      printf("\n Hexadecimal equivalent is %c.",hexaDec[j]);
   }
}
 int bintohexa(unsigned long binary)
 {
   unsigned long hexaval=0,remainder=0,i=1;
   while(binary!=0)
   {
      remainder=binary%10;
      hexaval=hexaval+(i*remainder);
      i=i*2;
      binary=binary/10;
   }
   printf("\n Hexadecimal equvalent is %lu",hexaval);
 }

 int main()
 {
     int number,choice;
     unsigned long binary;
    printf("\nChoose \n1.Binary \t2.Decimal\n ");
    scanf("%d",&choice);
    switch(choice)
    {
       case 1:
       printf("Enter binary number: ");
       scanf("%lu",&binary);
            bintohexa(binary);
            break;
      case 2:
       printf("Enter decimal number: ");
       scanf("%d",&number);
             dectohexa(number);
             break;
      default:
             printf("Wrong Choice!");
             break;               
    }
    return 0;
 }
```

# Explanation
Here I used two separate functions for decimal and binary numbers and takes the choice from the user that whether he/she wants to convert binary or decimal number.Due to lack of time I am unable to type more!!!
