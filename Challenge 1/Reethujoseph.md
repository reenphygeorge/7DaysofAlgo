#include<stdio.h>  
int main(){    
int n,i,r=0,flag=0;    
printf("Enter the number to check prime:");    
scanf("%d",&n);    
r=n/2;    
for(i=2;i<=r;i++)    
{    
if(n%i==0)    
{    
printf("Number is not prime");    
flag=1;    
break;    
}    
}    
if(flag==0)    
printf("Number is prime");     
return 0;  
 }    
 
 
 
 ////Explanation///
 
 
In the program, a for loop is iterated from i = 2 to i < n/2.
In each iteration, whether n is perfectly divisible by i is checked using:
                 if (n % i == 0) {
                   flag = 1;
                      break;
                       }
If n is perfectly divisible by i, n is not a prime number. In this case, flag is set to 1, and the loop is terminated using the break statement.
we have initialized flag as 0 during the start of our program.So, if n is a prime number after the loop, flag will still be 0. However, if n is a non-prime number,
flag will be 1.
