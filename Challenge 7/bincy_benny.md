# Code
```cpp
#include <iostream>

using namespace std;
void calc(int a,int b)
{
    int num1=b,num2=a,temp,lcm,hcf;
    if(a>b)
    ;
    else 
    {
    temp=a;
    a=b;
    b=temp;
    }
    while(b!=0)
    {
        hcf=b;
        b=a%b;
        a=hcf;   
    }
    cout<<"\n Largest no. which completely divides both these no.s: "<<hcf;
    lcm=(num1*num2)/hcf;
    cout<<"\n Smallest no. which is the product of these 2 no.s: "<<lcm;
}

int main()
{
    int a,b;
    cout<<"enter 2 numbers: ";
    cin>>a>>b;
    cout<<"\n "<<a<<"  "<<b;
    calc(a,b); return 0;
}

```

# Explanation
The user is asked to input 2 numbers.

*calc()* is called passing these 2 numbers as the parameters.
*'We know that the largest no.which completely divides both these numbers would be the
H.C.F and the smallest no. which is the product of these two numbers would be the L.C.M'.*

The 2 numbers are compared to find the largest among them so as to find the H.C.F(the 
biggest number is divided by the smallest as its divisor,then the remainder is taken as 
the divisor and the previous divisor as its dividend...this goes on till remainder equals
0,and this divisor finally is taken as the H.C.F)
Likewise L.C.M is found out by dividing the product of these 2 numbers with the H.C.F.

Finally the output is printed.
