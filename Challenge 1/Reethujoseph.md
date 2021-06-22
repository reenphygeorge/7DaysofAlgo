#code
```
  c 
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
 ```
 
 
#Explanation.
 
``` 
1.Read a no. from user.

2.To check whether its prime, the divisibility of the number(n) with numbers from i to n/i is checked (using for loop) as the numbers after n/2 will be divisible by those before n/2.If n is perfectly divisible by i,  then n is not a prime number. In this case, flag is set to 1, and the loop is terminated using the break statement.

3.we have initialized flag as 0 during the start of our program.So, if n is a prime number after the loop, flag will still be 0. However, if n is a non-prime number,
flag will be 1.Then we can check the number is prime or not.
```
