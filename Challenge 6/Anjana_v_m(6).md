# code
```python
def leapyear(days,hours,your_hours):
        final=float(hours/your_hours)
        i=1
        while (final < 1):
            final=final*i
            i += 1 
        return i
    
print ("How much time does your planet take to complete a revolution around your star or blackhole?")
print("Days :")
days=int(input())
print ("Hours :")
hours=int(input())
print("How many hours do you folks have in a day?")
your_hours=int(input())
leap=leapyear(days,hours,your_hours)
print("Your planet will have {} days in a year and a leap year every {} years".format(days,leap))
```
# Explanation
Here we have the function leapyear where days,hours and your_hours are the parameters.days and time represent how much time does your planet take to complete a revolution around
your star or blackhole in days and hours respectively.your_hours represents How many hours do you folks have in a day.leapyear function can help us  to find when leap year  occurs.
When inputs are provided properly,we get correct output
