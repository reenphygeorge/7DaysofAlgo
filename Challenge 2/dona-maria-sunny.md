##### Challenge 2: Spell it out.
##### Problem Statement: Implement a pure function that takes a whole number as an argument and returns the number in words. For eg. 26 would return a string ‘twenty six’.
##### Author: Dona Maria Sunny (S6, CSE)
# Code
```python
def spell_it(number):
    dict1={0: 'Zero', 1: 'One', 2: 'Two', 3: 'Three', 4: 'Four', 5: 'Five', 6: 'Six', 7: 'Seven', 8: 'Eight', 9: 'Nine', 10: 'Ten', 11: 'Eleven', 12: 'Twelve', 13: 'Thirteen',14: 'Fourteen', 15: 'Fifteen', 16: 'Sixteen', 17: 'Seventeen', 18: 'Eighteen',19: 'Nineteen', 20: 'Twenty', 30: 'Thirty', 40: 'Forty', 50: 'Fifty', 60: 'Sixty',70: 'Seventy', 80: 'Eighty', 90: 'Ninety'}
    length=len(str(number))
    if(number in dict1.keys()):
        return(dict1[number])
    elif(length==2):
        return(dict1[(number//10)*10] + " " + dict1[(number%10)])
    elif(length==3):
        marker=str(number)
        if(marker[1]=="0" and marker[2]=="0"):
            return(dict1[(number//100)] + " " + "Hundred")
        elif(marker[1]=="0"):
            return(dict1[(number//100)] + " " + "Hundred"+" and" + " " + dict1[(number%10)])
        elif(marker[2]=="0"):
            return(dict1[(number//100)] + " " + "Hundred"+" and" + " " + dict1[(number%100)])
        elif((number%100)>=11 and (number%100)<=19):
            return(dict1[(number//100)] + " " + "Hundred"+" and" + " " + dict1[(number%100)])
        else:
            marker=marker[1]
            return(dict1[(number//100)] + " " + "Hundred"+ " " + "and" + " " +dict1[(int(marker))*10]+  " "  + dict1[(number%10)])
    else:
        return("Invalid input!Enter a number in the range 0 - 999.")
        


number=int(input("Spell it out.\n Enter the whole number (0-999) whose words needed:"))
print(spell_it(number))
```
# Explanation
1. User enters the ```number``` whose words need to be displayed.
2. Entered ```number``` is passed to the function and now the function **spell_it** is called.
3. Inside the function **spell_it** the following happens :
   * If ```number``` is in dict1.keys() corresponding value is returned.
   * If length of ```number``` is 2 ```//``` and ```%``` operators are used to get the desired output.
   * If length of ```number``` is 3 certain cases are considered.
     Last two digits are zero.
     Middle digit is zero.
     Last digit is zero.
     Last two digits are between 11 and 19.
     All other cases.
     
     Using ```//``` and ```%``` operators required output is generated.
   * If a number not in the range 0 - 999 is entered **Invalid input!Enter a number in the range 0 - 999** is returned.
