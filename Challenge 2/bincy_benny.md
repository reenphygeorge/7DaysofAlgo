# Code
```cpp

#include<iostream>
#include<math.h>
using namespace std;

int wording(int num)
{
  char error='t';
    switch(num)
    {
        case 1:cout<<" ONE ";break; 
        case 2:cout<<" TWO ";break;
        case 3:cout<<" THREE ";break;
        case 4:cout<<" FOUR ";break;
        case 5:cout<<" FIVE ";break;
        case 6:cout<<" SIX ";break;
        case 7:cout<<" SEVEN ";break;
        case 8:cout<<" EIGHT ";break;
        case 9:cout<<" NINE ";break;
        case 10:cout<<" TEN ";break;
        
        case 11:cout<<"ELEVEN ";break;
        case 12:cout<<"TWELVE ";break;
        case 13:cout<<"THIRTEEN ";break;
        case 14:cout<<"FOURTEEN ";break;
        case 15:cout<<"FIFTEEN ";break;
        case 16:cout<<"SIXTEEN ";break;
        case 17:cout<<"SEVENTEEN ";break;
        case 18:cout<<"EIGHTEEN ";break;
        case 19:cout<<"NINETEEN ";break;

        case 20:cout<<" TWENTY ";break;
        case 30:cout<<" THIRTY ";break;
        case 40:cout<<" FOURTY ";break;
        case 50:cout<<" FIFTY ";break;
        case 60:cout<<" SIXTY ";break;
        case 70:cout<<" SEVENTY ";break;
        case 80:cout<<" EIGHTY ";break;
        case 90:cout<<" NINETY ";break;
        case 100:cout<<" HUNDRED ";break;
        case 1000:cout<<" THOUSAND";break;
        case 100000:cout<<" LAKHS ";break;
        case 10000000:cout<<" CRORES";break;
        default:error='f';
    }
    return(error);

}
int numToText(int num)
{
    int c=0;
    int temp1;int temp,temp2;
    char error;
    int n=num;
    while(n!=0)
    {
    n/=10;
    c++;
    }
    double d=0;
    d=c-1;
    int p;
    p=pow(10.0,d);

 for(int i=c;i>=3;i--)
    {
        temp1,temp,temp2=0;
        temp=num/p;
        reiterate:
        if (c==5||c==7||c==9)
        {
         p/=10;
         temp1=temp2=num/p;
         wording(temp1);
         temp1/=10;
         temp1*=10;
         wording(temp1);
         temp2-=temp1;
         wording(temp2);
         wording(p);
         num=num-temp2*p-temp1*p;
         c-=2;d-=2;
         p/=10;
        }
        if(c==5||c==7)
        goto reiterate;
        temp=num/p;
        if(num==0)
        break;
        wording(temp);
        cout<<" ";
        wording(p);
        num=num-temp*p;
        if(num==0)
        break;
        cout<<" AND ";
        c--;d--;
        p=pow(10.0,d);
        if(c<=2)
        break;
    }  
 if(c==2)
    {
        error =wording(num);
        if (error=='f')
        {
        temp1=num/10;
        temp1*=10;
        wording(temp1);
        num-=temp1;
        c--;d--;p=pow(10.0,d);
        }
        else 
         c-=2;
        
    }
        if(c==1)
       wording(num);
 return 0;
}


int main()
{
    int num;
    char error='t';
    cout<<"enter a no.\n";
    cin>>num;
    error=wording(num);
     if(error=='f')
    {
    numToText(num);
    }
    return 0;
}
```

# Explanation
**Functions used:**
* *wording()*:contains text forms of numerals i.e our dictionary of conversion.
* *numToText()*:splits the number into its 10s,100s...etc place wherever necessary and prints the output methodically.
* *main()*:gets input from the user and calls wording(),numToText() accordingly.

P.S:I'll admit that this program might not be efficient and probably will need changes.😞
