# CODE
~~~python
def leap(days,hours,time):
    count=0
    chour=hours
    while(hours!=time):
        hours=hours+chour
        count+=1
    print("Your planet will have",+days,"days in a year and a leap year every",+(count+1),"years.")


print("How much time does your planet take to complete a revolution around your star or blackhole?")
days=int(input("Days:\t"))
hours=int(input("hours:\t"))
time=int(input("How many hours do you folks have in a day?\n"))
leap(days,hours,time)
~~~

# EXPLANATION
  *The days and hours required for the revolution are taken from the user in the main function
  *The duration of a day is also taken from the user and these 3 values are passed to the function leap
  *Count value is set to 0
  *Condition is checked if the day duration is not equal to the hours then count is  incremented by 1 and hour value is increased
  *When the hours value is equal to the day duration looping stops and we get the value for the leap year
  *Leap year is calculated by the adding the remaining hours of the revolution period . when the sum id equal to the day duration an extra day is added to the year(Leap Year)
