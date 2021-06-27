# Code
```
#Python Code
#Problem Statement : Write a pure function that takes the duration an imaginary planet takes to revolve around it's star or blackhole (in days and hours, for example 365 and 5 hours) as an input and determines how many days a year should the planet have and subsequently it's leap year rule.
#Author : Akshara Raju

def planet_days(days,hours,day):
    try:
        if days == 0:
            return("Invalid Input!!!")
        if day == 0:
            return ("Invalid Input!!!")
        if hours == 0:
            return("Your planet will have {} days in a year and no leap year".format(days))
        if hours >= day:
            return("invalid Input!!!")
        else:
            leap_year = day//hours
            return("Your plane will have {} days in a year and a leap year every {} years".format(days,leap_year))
    except:
        return("Invalid!!!")        
        

print("How much time does your planet take to complete a revolution around your star or blackhole?")
days = int(input("Days : "))
hours = int(input("Hours : "))
print("How many hours do you have a day?")
day = int(input())
print(planet_days(days,hours,day))



          


     


```

# Explanation
The inputs **days** , **hours** , **day** are passed as an argument to the function **planet_days**. The it checks some conditions such as- number of days a year or hours a day shouldn't be 0,
hours cannot be greater than hours a day as it will invalidate the number of days a year already mentioned. If right inputs are provided, output will be displayed.
