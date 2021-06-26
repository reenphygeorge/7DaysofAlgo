# Code
```
print("How much time does your planet take to complete a revolution around your star or blackhole?")
days=int(input("Days : "))
hrs=int(input("Hours : ")) 
dayhr=int(input("How many hours do you folks have in a day?"))
leap=dayhr//hrs
c=1
while(leap<1):
       leap=leap*c
       c+=1
print("Your planet will have",+days,"days in a year and a leap year every",+leap,"years.")

```

# Explanation
 - Enter the number of days,hours and the hours in a day.
 - calculate the number of leap year by dividing day hours with hours.
 - put c=1
 - while leap<1
    - leap= leap we got * c
    - increment c
 - print the result
