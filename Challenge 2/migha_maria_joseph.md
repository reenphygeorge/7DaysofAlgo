# code

```python
def spell_item(num):
    lis1=[" ", "one", "two", "three","four", "five", "six", "seven","eight", "nine","ten", "eleven", "twelve","thirteen", "fourteen","fifteen","sixteen","seventeen","eighteen","nineteen"]
    lis2=["", "", "twenty", "thirty", "forty","fifty", "sixty", "seventy", "eighty","ninety"]
    if num==0:
        return "Zero"
    elif num<=19:
        return lis1[num]
        
    elif num<=99:
        return lis2[num//10]+" "+lis1[num%10]
    elif num<=999:
        div=num%100
        value=lis2[div//10]+" "+lis1[div%10]
        return lis1[num//100]+" "+"hundred"+ " "+value
    else:
        return "please a number between 0 and 999"
num=int(input())
result=spell_item(num)
print(result)


```
# Explanation

 1. Here given  two lists of index up to 10 ie lis1 and lis2
 2. If the number given is 0, the output will be direct
 3. If the number given is less than 19,we can take directly from lis1
 4. If the number given is less than 99, first take the quotient of given number and point to the index of lis2 and join with remainder of given number which points to the index     of lis1
 5. If the number given is less than 999, first take the remainder of given number and  then take the quotient of that remainder and point to the index of lis2 and join with remainder of that remainder, which points to the index of lis1 and get stored in a variable named value
 
    5.1  Then combine value, with the quotient of given number  and point to the index of lis1
 
