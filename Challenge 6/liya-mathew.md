# Code
```python3
def calculate_days(days, extrahours, dayhours):
    decimal_sum = 0.0
    accurate_days = (days * dayhours + extrahours) / dayhours
    decimal = round(accurate_days - days, 2)
    decimal_sum = decimal_sum + float(decimal)
    count = 1
    while (decimal_sum - int(decimal_sum) != 0):
        count += 1
        decimal_sum = decimal_sum + decimal
    no_of_leapyears = decimal * count
    return no_of_leapyears, count


print("How much time does your planet take to complete a revolution around your star or blackhole?")
print("Days:")
days = int(input())
print("Hours:")
hours = int(input())
print("How many hours do you folks have in a day?")
dayhours = int(input())
no_ofleapyear, count = (calculate_days(days, hours, dayhours))
print("Your planet will have {} days in a year and {} leap years in every {} years".format(days, int(no_ofleapyear), count))

```

# Explanation
We need to implement a function to determine how many days an year should an imaginary planet have and subsequently it's leap year rule.
* For this firstly, we ask the user to enter the duration of year in terms of days and hours(1 complete revolution= 1 year).Then we request the user to enter the number of hours in a day and pass all these values as arguments of our function.
* From the input details we calculate the exact no of days in an year (fractional form).Then we extract the decimal portion of it and try to convert it into a whole number by adding it continuosly until it forms a whole number.The number of times addition is performed is monitored by count variable and the product of count and extracted decimal gives the frequency of leap years. Both the count and no_of_leapyear is returned.
* The logic for this program is based on how many years are required to compensate the fractional part of the actual number of days in an year.
# OUTPUT
How much time does your planet take to complete a revolution around your star or blackhole?
Days:
365
Hours:
6
How many hours do you folks have in a day?
24
Your planet will have 365 days in a year and 1 leap years in every 4 years



