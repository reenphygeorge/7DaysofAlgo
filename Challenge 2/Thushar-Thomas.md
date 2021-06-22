# Code
```python
'''
Documentation
Program to covert number to words

Name   : Thushar Thomas
Branch : AI & DS
'''
def spell_it(num): # Function to convert number to words
    i=0 
    l=len(num) # Checks the number of digits of the given number
    p=0
    if (l == 0): # If no number is entered by the user
        print("No number entered")
        return
    if (l > 4): # If the number exceeds 4 digits
        print("5 or more Digit numbers are not supported")
        return
    num=int(num)
    one_digits = ["", "one", "two", "three","four", "five", "six", "seven","eight", "nine"]
    two_digits = ["", "ten", "eleven", "twelve","thirteen", "fourteen", "fifteen","sixteen", "seventeen", "eighteen","nineteen"]
    tens_multiple = ["", "", "twenty", "thirty", "forty","fifty", "sixty", "seventy", "eighty","ninety"]
    tens_power = ["","hundred","", "thousand"]
    if num==0:
        print("Zero")
        return
    if l==1:
        print(one_digits[num])
    if l==2:
        if 10<num<20:
            print(two_digits[num-9])
        else:
            print(tens_multiple[int(num/10)>0],one_digits[num%10])
    if l==3:
        if 9<num%100<20:
            print(one_digits[int(num/100)],tens_power[int(num/100)%10>0],two_digits[int(num%10)+1])
        else:
            print(one_digits[int(num/100)],tens_power[int(num/100)%10>0],tens_multiple[int((num%100)/10)],one_digits[num%10])
    if l==4:
        if 9<num%100<20:
            print(one_digits[int(num/1000)],tens_power[(int(num/1000)>0)+2],one_digits[int((num%1000)/100)],tens_power[int(num/100)%10>0],two_digits[int(num%10)+1])
        else:
            print(one_digits[int(num/1000)],tens_power[(int(num/1000)>0)+2],one_digits[int((num%1000)/100)],tens_power[int(num/100)%10>0],tens_multiple[int((num%100)/10)],one_digits[num%10])
n=input("Enter a number:") # Takes input from the user
spell_it(n)
```

# Explanation
The program above gets a number from the user and converts it to words. 
<p>In this progam we can convert upto a 4 digit number to words. 
    This program also considers teen numbers.
    \nThis program has resolved the error with the position of 0 in the 4 digit number given below
      '0001', '0010', '0100'</p>
 Thank you
