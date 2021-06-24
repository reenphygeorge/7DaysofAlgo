# Code
```cpp

#include<iostream>
#include<math.h>
using namespace std;

int convert_Tobase16(int num,char choice)
{
    char hex[50];
    int i=0;
 reiterate:
if(choice=='d')
{
     int temp;
  
   while(num!=0)
    {
        temp=num%16;
        if(temp<10)
        hex[i]=temp+48;        
        else   
        hex[i]=temp+55;
        i++;
        num=num/16;
    } 
}    for (int j = i - 1; j >= 0; j--)
        cout << hex[j];


if(choice=='b')
{
    int c=0,decimal=0;
    int n=num;
    double j=0;
    int temp1,p=0;
    
   
while(n)
    {
         temp1=n%10;
         p=pow(2.0,j);
         temp1*=p;
         decimal=decimal+temp1;
         ++j;
         n/=10;
    }
    choice='d';
    num=decimal;
    goto reiterate;
}
 return 0;
}

int main()
{
    int num;
    char choice;
    cout<<"WHICH ONE WOULD YOU LIKE TO CONVERT:\n\tBINARY\n\tDECIMAL\n**(press b/d)\t";
    cin>>choice;
    cout<<"Enter a no.\n";
    cin>>num;
    convert_Tobase16(num,choice);
    return 0;
}
```

# Explanation
**The user is allowed to choose whether to convert decimal/binary to hexadecimal format.**

*convert_Tobase16()*:converts 

                      * decimal -> hexadecimal
                        *this conversion takes place by dividing the user given input
                        repeatedly by 16 ,storing the remainders in their respective 
                        ASCII values and finally displaying it in the reverse form.
                        
                      * binary -> decimal -> hexadecimal
                        *here binary is first converted into decimal by multiplying 
                        the digits with 2 raised to some exponent value starting from
                        0 and thereby incrementing it further.Lastly, it is converted 
                        into hexadecimal using the same method mentioned above.
                      
                    
                      
