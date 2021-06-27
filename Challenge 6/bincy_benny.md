# Code
```cpp
#include <iostream>
using namespace std;
int leapyr(int days,float extra_hrs,int hrs)
{
    float leapyr_ct,exact_lpyr;
    int temp,whole_yr;
    cout<<"\nYour planet will have exact "<<days<<" days in a year";
    if (extra_hrs==0)
    cout<<"\nno leap years required";
    leapyr_ct=hrs/extra_hrs;
     whole_yr=int(leapyr_ct);
    float decimal_pt=leapyr_ct-whole_yr;
    if(decimal_pt>0.5)
    {
        temp=whole_yr+1;
        exact_lpyr=hrs/(temp-leapyr_ct);
        cout<<"\nYour planet will have a leap year in every "<<temp<<" years and in every "<<exact_lpyr<<" years";
    }    
    else if(decimal_pt<0.5&&decimal_pt!=0)
    {
        temp=whole_yr;
        exact_lpyr=hrs/(decimal_pt*10);
        cout<<"\nYour planet will have a leap year in every "<<temp<<" years and in every "<<exact_lpyr<<" years";
    }    
    
    if(decimal_pt==0)
    cout<<"\n And a leap year in every "<<int(leapyr_ct)<<" years";
    return 0;
}

int main()
{
    int days,hrs;
    float extra_hrs;
    cout<<"How much time does your planet take to complete a revolution around your star or blackhole?\nDays:";
    cin>>days;
    cout<<"\nhours:";
    cin>>extra_hrs;
    cout<<"\nhow many hours do you folks have in a day: ";
    cin>>hrs;
    leapyr(days,extra_hrs,hrs);
    return 0;
}

```

# Explanation
The user is asked to input the the time taken by one revolution in days and hrs(which would be the no.of days in a year) and also the total no. of hours in a day.
In *leapyr()*,the total no. of days is divided by the extra hours to get the occurences of leap year.
If it's not a whole no. then it is rounded off,the remaining decimal value gets evaluated again to find the occurence of the leap year.
And finally the The total no. of days in a year and the occurences of leap year gets displayed.

**P.S**
*I've done the coding in such a way that the leap year would always have +1 day extra than the normal year.So if the leap year encounters a  decimal part,
rather than adding that to no.of days in a leap year,I've made changes to the occurences of leap yr.* 
