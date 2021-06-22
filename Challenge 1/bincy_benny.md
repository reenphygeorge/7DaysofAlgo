# Code
```
#include<iostream>
#include<math.h>
using namespace std;
int checkprime(int num)
{
    int c=0;
    for(int i=2;i<=sqrt(num);i++)
    {
    if(num%i==0)
    c++;
    }
    if (num==1)
    cout<<"FALSE\t:"<<num<<" is Not PRIME";
    if(c>1)
    cout<<"FALSE\t:"<<num<<" is Not PRIME";
    else 
    cout<<"TRUE\t:"<<num<<" is PRIME";
    return 0;
}
int main()
{
int n;
cout<<"Enter a number:\n";
cin>>n;
checkprime(n);
return 0;
}
```

# Explanation
**Overall Workflow**:When a user inputs a number (say *num*),a fn **_checkprime()_** is called with *num* as its parameter.Then **_checkprime()_**
checks whether the no. is infact a prime or not by returning TRUE if it is, otherwise it returns FALSE.

**Checkprime()**:This fn contains a for loop where i is initialised to 2 and gets iterated until its greater than the sqrt of *num* (less cumbersome 
method than to check all the way to *num* or even half of it ,as a no. which is not prime can be expressed as factors less than the sqrt of the said no. 
,so if *num* cannot be divisible by any of these no.s less than sqrt(num),it has to be a PRIME no.).
The if condition checks whether *num* is divisible by any other no. and increments the variable c if it is.Outside the loop ,there's yet another 
condition as the previous loop iterates from 2 .If it's 1 then FALSE is printed as the output,for the variable c>1 ,it displays FALSE (as the no. 
is divisible by numbers other than itself excluding 1) and prints TRUE otherwise(prime no. only has 1 and the no. itself as a factor,so it should 
have only one factor excluding 1).

