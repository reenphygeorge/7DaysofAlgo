# Code
```python
def leap_year(days,hours,day_hours):
    result=float(hours/day_hours)
    count=1
    while(result<1) :
    	result=result*count
    	count=count+1
    return count
print("How much time does your planet take to complete a revolution around your star or blackhole?")
print("Days:",end="")
days = int(input())
print("Hours:",end="")
hours = int(input())
print("How many hours do you folks have in a day?")
day_hours = int(input())
count1=leap_year(days, hours, day_hours)
print("Your planet will have {} days in a year and a leap year every {} years".format(days,count1))
```
# Explanation
1. Write a pure function that takes the duration an imaginary planet takes to revolve around it's star or blackhole (in days and hours, for example 365 and 6 hours) as an input and determines how many days a year should the planet have and subsequently it's leap year rule
2. In the Input they asked to, How much time does your planet take to complete a revolution around your star or blackhole?(ie Days:365,Hours:6) and to input how many hours do you folks have in a day?(ie 24)
3. Then the output should be, Your planet will have 365 days in a year and a leap year every 4 years,the basic logic of the program is to find days a year should the planet have and subsequently it's leap year rule
    


