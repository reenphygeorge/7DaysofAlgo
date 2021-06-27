##### Challenge 6: Suns, blackholes and leap years.
##### Problem Statement: Write a pure function that takes the duration an imaginary planet takes to revolve around it's star or blackhole (in days and hours, for example 365 and 5 hours) as an input and determines how many days a year should the planet have and subsequently it's leap year rule.
##### Your program should work something like this:
_How much time does your planet take to complete a revolution around your star or blackhole?_

_Days  : 365_

_Hours : 6_

_How many hours do you folks have in a day?_

_24_

_Your planet will have 365 days in a year and a leap year every 4 years._

##### Author: Dona Maria Sunny (S6, CSE)
##### Language used: Python 3
# Code
```python
def myFunction(hours, hoursInOneDay ,days ):
    if(days==0 and hours==0):
        return("Invalid input! Enter days and hours.")
    elif(days==0):
        return("Your planet will have {} hours in a year and NO leap year.".format(hours))
    elif(hours==0):
        return("Your planet will have {} days in a year and NO leap year.".format(days))
    else:
        leapYearCount=(hoursInOneDay//hours)
        return("Your planet will have {} days in a year and a leap year every {} years.".format(days,leapYearCount))

    

print("How much time does your planet take to complete a revolution around your star or blackhole?")
try:
    days=int(input("Days : "))
    hours=float(input("Hours : "))
    hoursInOneDay=float(input("How many hours do you folks have in a day?"))
    print(myFunction(hours, hoursInOneDay, days))
except:
    print("Invalid input! Enter a whole number for Days.")


```
# Explanation
1. User enters the ```days```, ```hours``` and ```hoursInOneDay```. ***Try except*** is used to handle error caused if ```days``` is not of type int. 
2. Now the function **myFunction()** is called. ```days```, ```hours``` and ```hoursInOneDay``` are passed to it.
3. Inside the function the following happens:
   * If both ```days``` and ```hours``` are 0, then ***Invalid input! Enter days and hours*** statement is returned.
   * Else if ```days``` is 0, then hours in a year and NO leap year is returned.
   * Else if ```hours``` is 0, then days in a year and NO leap year is returned.
   * Else, ***hoursInOneDay//hours*** is done. Days in a year and occurence of leap year after how many years is returned in this case. 
