# Code
```
def calculate_days_and_leap_year():
    print("How much time does your planet take to complete a revolution around your star or blackhole?")
    days=int(input("Days :"))
    hours=float(input("Hours :"))
    print("How many hours do you folks have in a day?")
    per=int(input())
    total=((days*per)+hours)/per
    days_in_year=int(total)
    roun=round(total,2)
    frac=roun%1
    if frac==0:
        leap=0
    else:
        for i in range(101):
            val=frac*i
            if round(val,2)==1.00:
                leap=i
                break
            if round(val,2)>1:
                leap=i-1
                break
    print("Your planet will have "+str(days_in_year)+" days in a year and a leap year every "+str(leap)+" years.")

calculate_days_and_leap_year()
```

# Explanation
The function calculate_days_and_leap_year is used to find the no of the days and leap years required according to the revolution of our planet. 
So for this we ask the user to input the no of days and extra hours used by our planet for revolution. The user has to input the hours per day in our planet .
Then calculate total hours of revolution which is then divided by hours per day which gives total(a float value). The integer part of this total is the no of days in a year. 
Now we round the total to 2 decimal value and the decimal part is extracted. if the decimal part is 0 then leap is 0. Else we implement a for loop to find the leap year. 
In the loop, we multiply the decimal part with the i which is incremented during each loop. The value obtained is rounded to 2 decimal places and if that rounded value is 
1.00 then we assign leap as i or if the rounded value is greater than 1 then we assign leap as i-1. Finally at the end of the function we print the results. 
