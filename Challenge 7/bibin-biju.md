Code
===
```cpp

#include<iostream>
using namespace std;
int hcf_lcm(int number1,int number2)
{
    int i=0,HCF,LCM;
    for(i=1;i<=number1;i++)
    {
        if((number1%i==0) && (number2%i==0))
        {
            HCF=i;
        }
    }
    LCM=(number1*number2)/HCF;
    cout<<"HCF = "<<HCF;
    cout<<" LCM = "<<LCM;
    
}
int main()
{
    int number1,number2;
    cout<<"Enter first number: ";
    cin>>number1;
    cout<<"Enter second number: ";
    cin>>number2;
    hcf_lcm(number1,number2);
    return 0;
}
```
Explanation
===
1.Read the numbers from user.

2.In the user defined function,the increment value i checks from initial set condition to the first number(can also use second number) and HCF is the value 
which is obtained as the common value of modulus operation of first and second number with i when remainder equals to 0.

3.LCM is obtained by (number1*number2)/HCF and we print the values obtained.
