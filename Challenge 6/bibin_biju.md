Code
===
```c
#include<stdio.h>
float leapYear(float days,float hours,float hrs) 
{
    float YrValue,leapYr;
    YrValue=hrs/hours;
    for(YrValue=YrValue;YrValue<1;YrValue++)
    {
    leapYr=1/YrValue;
    }
    printf("\nYour planet will have %.0f days in a year and a leap year in every %.0f years.",days,leapYr);

}  
int main()
{
    float days,hrs,hours,leapYr;
    float YrValue=0;
    printf("\nHow much time does your planet take to complete a revolution around your star or blackhole?\nDays:  ");
    scanf("%f",&days);
    printf("Hours: ");
    scanf("%f",&hrs);
    printf("\nHow many hours do you folks have in a day?\n ");
    scanf("%f",&hours);
    leapYear(days,hours,hrs);
    return 0;
}
```
Explanation
===
1.Here the user inputs all inputs.

2.We divide the extra hours by total hours in a day which is less than 1.

3.Then we add that value to itself a number of times until it becomes less than or equal to 1.

4.This particular count is actually the years in which a leap year occurs. 

