# Code
```python
'''
Documentation
Program to return days and leap year of a imaginary planet

Name   : Thushar Thomas
Branch : AI & DS
'''
def year(D,H,h):    # Function to calculate the leap year of a planet
    while H>=h:    # If hours of revolution is more than the hours in a day
        D+=1
        H-=h
    print("Your planet will have",D,"days in a year",end=" ")
    if H!=0:    # If the entered hour constitute a day or not
        leap_year=int(h/H)
        if H>=(h/2):
            leap_year=(h/(h-H))
            print("and a leap year every",leap_year,"years.")
        elif H<(h/2):
            leap_year=(h/H)
            print("and a leap year every",leap_year,"years.")
        else:
            print("and no leap year.")
    else:
        print("and no leap year.")
print("How much time does your planet take to complete a revolution around your star or blackhole?")
Days=int(input("Days: "))
Hours=int(input("Hours: "))
hours=int(input("How many hours do you folks have in a day?\n"))
year(Days,Hours,hours)    # Calling the function
```

# Explanation
#### In this program, user can enter the days and hours of revolution of an imaginary planet and gets it's leap year.
<p> <br/><br/>Error in consideration: Working on the convertion of decimal values of leap year to corresponding hours.
   
<br/>Thank you
